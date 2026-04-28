#### Description

The `pinterest` command provides a CLI interface to the Pinterest API v5. It supports managing pins, boards, board sections, searching, user account info, and media uploads.

All API calls are authenticated using a stored access token. Run `aux4 pinterest login --token YOUR_TOKEN` to authenticate before using other commands.

By default, commands use the production API. Set `--apiUrl https://api-sandbox.pinterest.com` or the `PINTEREST_API_URL` environment variable to use the sandbox.

Available subcommands: `login`, `logout`, `status`, `pin`, `board`, `search`, `user`, `media`.

#### Usage

```bash
aux4 pinterest <subcommand>
```

#### Example

```bash
aux4 pinterest login --token pina_ABCDEF123456
aux4 pinterest user info
aux4 pinterest pin list
aux4 pinterest board list
```
