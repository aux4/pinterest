#### Description

The `followers` command lists the authenticated user's followers.

#### Usage

```bash
aux4 pinterest user followers [--pageSize <n>] [--bookmark <token>] [--tokenFile <path>]
```

--pageSize    Number of followers to return (default: 25, max: 100)
--bookmark    Pagination bookmark from previous response
--tokenFile   Custom token file path

#### Example

```bash
aux4 pinterest user followers --pageSize 10
```

```text
{"items":[{"username":"janedoe"}],"bookmark":"Pz9..."}
```
