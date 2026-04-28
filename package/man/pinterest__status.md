#### Description

The `status` command displays the current Pinterest authentication status, including whether the token is valid or expired, granted scopes, and expiry time.

#### Usage

```bash
aux4 pinterest status
```

#### Example

```bash
aux4 pinterest status
```

```text
Provider:      pinterest
Status:        valid
Scopes:        boards:read,boards:write,pins:read,pins:write,user_accounts:read
Expires at:    2026-04-28T12:30:00Z
Refresh token: yes
Token file:    .oauth/pinterest.json
```
