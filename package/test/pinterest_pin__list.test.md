# pinterest pin list

## with mock API

```beforeAll
nohup python3 -c "
from http.server import HTTPServer, BaseHTTPRequestHandler
import json

class Handler(BaseHTTPRequestHandler):
    def do_GET(self):
        auth = self.headers.get('Authorization', '')
        if not auth.startswith('Bearer '):
            self.send_response(401)
            self.end_headers()
            return
        if self.path.startswith('/v5/pins'):
            response = json.dumps({'items': [{'id': '123', 'title': 'Test Pin'}], 'bookmark': 'next123'})
        else:
            self.send_response(404)
            self.end_headers()
            return
        self.send_response(200)
        self.send_header('Content-Type', 'application/json')
        self.end_headers()
        self.wfile.write(response.encode())
    def log_message(self, format, *args):
        pass

HTTPServer(('', 18941), Handler).serve_forever()
" >/dev/null 2>&1 &
echo $! > /tmp/aux4-pinterest-pin-list-server.pid
sleep 1

mkdir -p .oauth
cat > .oauth/pinterest.json << 'ENDTOKEN'
{
  "clientId": "test-client",
  "clientSecret": "test-secret",
  "authUrl": "https://www.pinterest.com/oauth/",
  "tokenUrl": "https://api.pinterest.com/v5/oauth/token",
  "scopes": "pins:read",
  "accessToken": "mock-token",
  "refreshToken": "mock-refresh",
  "expiresAt": "2099-12-31T23:59:59Z"
}
ENDTOKEN
```

```afterAll
kill $(cat /tmp/aux4-pinterest-pin-list-server.pid) 2>/dev/null
rm -f /tmp/aux4-pinterest-pin-list-server.pid
rm -rf .oauth
```

### should list pins

```execute
aux4 curl auth-request --provider pinterest http://localhost:18941/v5/pins
```

```expect:json
{
  "items": [
    {
      "id": "123",
      "title": "Test Pin"
    }
  ],
  "bookmark": "next123"
}
```
