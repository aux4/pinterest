#### Description

The `list` command retrieves all sections for a specific board.

#### Usage

```bash
aux4 pinterest board section list <boardId> [--pageSize <n>]
```

--pageSize    Number of sections to return (default: 25, max: 100)

#### Example

```bash
aux4 pinterest board section list 123456
```

```text
{"items":[{"id":"789012","title":"Favorites"}]}
```
