#### Description

The `pinterest` command provides a CLI interface to the Pinterest API v5. It supports managing pins, boards, board sections, searching, user account info, and media uploads.

All API calls are authenticated using OAuth2 via `aux4/curl`. Run `aux4 pinterest login` to authenticate before using other commands.

Available subcommands: `login`, `logout`, `status`, `pin`, `board`, `search`, `user`, `media`.

#### Usage

```bash
aux4 pinterest <subcommand>
```

#### Example

```bash
aux4 pinterest login --clientId abc123 --clientSecret secret
aux4 pinterest pin list
aux4 pinterest board list
```
