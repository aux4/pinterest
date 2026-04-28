#### Description

The `info` command retrieves the authenticated user's Pinterest account information, including username, account type, and profile details.

#### Usage

```bash
aux4 pinterest user info [--tokenFile <path>]
```

--tokenFile   Custom token file path

#### Example

```bash
aux4 pinterest user info
```

```text
{"username":"johndoe","account_type":"BUSINESS","profile_image":"https://..."}
```
