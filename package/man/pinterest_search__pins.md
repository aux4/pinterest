#### Description

The `pins` command searches the authenticated user's pins by keyword.

#### Usage

```bash
aux4 pinterest search pins <query> [--pageSize <n>]
```

--pageSize    Number of results to return (default: 25, max: 100)

#### Example

```bash
aux4 pinterest search pins "summer recipes"
```

```text
{"items":[{"id":"123","title":"Summer Pasta"}],"bookmark":"Pz9..."}
```
