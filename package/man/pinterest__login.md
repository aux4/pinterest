#### Description

The `login` command authenticates with Pinterest using OAuth2. It wraps `aux4 curl oauth login` with Pinterest-specific defaults for the authorization and token URLs.

After running this command, a browser URL is displayed. Open it, authorize the app, and the token is saved locally to `.oauth/pinterest.json` (or a custom path via `--tokenFile`).

The default scopes are `boards:read,boards:write,pins:read,pins:write,user_accounts:read`. Override with `--scopes` if you need different permissions.

#### Usage

```bash
aux4 pinterest login --clientId <id> --clientSecret <secret> [--scopes <scopes>] [--callbackPort <port>] [--tokenFile <path>]
```

--clientId       Pinterest app client ID
--clientSecret   Pinterest app client secret
--scopes         OAuth scopes (default: boards:read,boards:write,pins:read,pins:write,user_accounts:read)
--callbackPort   Local callback port (default: 9876)
--tokenFile      Custom token file path (default: .oauth/pinterest.json)

#### Example

```bash
aux4 pinterest login --clientId abc123 --clientSecret mysecret
```

```text
Open this URL in your browser to authorize:

https://www.pinterest.com/oauth/?client_id=abc123&redirect_uri=http://localhost:9876/callback&response_type=code&scope=boards:read,boards:write,pins:read,pins:write,user_accounts:read&state=1234567890

Waiting for callback on port 9876...
Login successful! Token saved to .oauth/pinterest.json
```
