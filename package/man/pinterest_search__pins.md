#### Description

The `pins` command searches the authenticated user's pins by keyword.

#### Usage

```bash
aux4 pinterest search pins <query> [--pageSize <n>] [--bookmark <token>] [--tokenFile <path>]
```

--pageSize    Number of results to return (default: 25, max: 100)
--bookmark    Pagination bookmark from previous response
--tokenFile   Custom token file path

#### Example

```bash
aux4 pinterest search pins "summer recipes"
```

```text
{"items":[{"id":"123","title":"Summer Pasta"}],"bookmark":"Pz9..."}
```
