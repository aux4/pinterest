#### Description

The `login` command stores your Pinterest API access token locally. Get your token from the [Pinterest Developer Console](https://developers.pinterest.com/) under your app settings. The token starts with `pina_`.

The token is saved to `.oauth/pinterest.json` in the current directory. Add `.oauth/` to your `.gitignore` to avoid committing credentials.

#### Usage

```bash
aux4 pinterest login --token <access-token>
```

--token   Pinterest API access token (required)

#### Example

```bash
aux4 pinterest login --token pina_ABCDEF123456
```

```text
Token saved to .oauth/pinterest.json
```
