#### Description

The `list` command retrieves the authenticated user's boards, including group boards where the user is a collaborator.

#### Usage

```bash
aux4 pinterest board list [--pageSize <n>] [--bookmark <token>] [--tokenFile <path>]
```

--pageSize    Number of boards to return (default: 25, max: 100)
--bookmark    Pagination bookmark from previous response
--tokenFile   Custom token file path

#### Example

```bash
aux4 pinterest board list
```

```text
{"items":[{"id":"123456","name":"Travel Ideas"}],"bookmark":"Pz9..."}
```
