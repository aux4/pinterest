# pinterest status

## with valid token

```beforeAll
mkdir -p .oauth
cat > .oauth/pinterest.json << 'ENDTOKEN'
{
  "clientId": "test-client",
  "clientSecret": "test-secret",
  "authUrl": "https://www.pinterest.com/oauth/",
  "tokenUrl": "https://api.pinterest.com/v5/oauth/token",
  "scopes": "boards:read,boards:write,pins:read,pins:write,user_accounts:read",
  "accessToken": "test-token",
  "refreshToken": "test-refresh",
  "expiresAt": "2099-12-31T23:59:59Z"
}
ENDTOKEN
```

```afterAll
rm -rf .oauth
```

### should show valid status

```execute
aux4 curl oauth status pinterest
```

```expect:partial
Provider:      pinterest
Status:        valid
Scopes:        boards:read,boards:write,pins:read,pins:write,user_accounts:read
```
