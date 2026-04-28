#### Description

The `list` command retrieves all sections for a specific board.

#### Usage

```bash
aux4 pinterest board section list <boardId> [--pageSize <n>] [--bookmark <token>] [--tokenFile <path>]
```

--pageSize    Number of sections to return (default: 25, max: 100)
--bookmark    Pagination bookmark from previous response
--tokenFile   Custom token file path

#### Example

```bash
aux4 pinterest board section list 123456
```

```text
{"items":[{"id":"789012","title":"Favorites"}]}
```
