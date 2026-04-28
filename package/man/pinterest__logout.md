#### Description

The `logout` command removes the stored Pinterest OAuth token. This does not revoke the token on Pinterest's side. To fully revoke access, visit your Pinterest app settings.

#### Usage

```bash
aux4 pinterest logout [--tokenFile <path>]
```

--tokenFile   Custom token file path (default: .oauth/pinterest.json)

#### Example

```bash
aux4 pinterest logout
```

```text
Logged out from pinterest
```
