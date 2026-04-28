#### Description

The `followers` command lists the authenticated user's followers.

#### Usage

```bash
aux4 pinterest user followers [--pageSize <n>]
```

--pageSize    Number of followers to return (default: 25, max: 100)

#### Example

```bash
aux4 pinterest user followers --pageSize 10
```

```text
{"items":[{"username":"janedoe"}],"bookmark":"Pz9..."}
```
