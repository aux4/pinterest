#### Description

The `create` command creates a new section within a board.

#### Usage

```bash
aux4 pinterest board section create <boardId> --body <json> [--tokenFile <path>]
```

--body        Section data as JSON (title)
--tokenFile   Custom token file path

#### Example

```bash
aux4 pinterest board section create 123456 --body '{"title":"Favorites"}'
```

```text
{"id":"789012","title":"Favorites"}
```
