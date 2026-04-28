#### Description

The `boards` command searches the authenticated user's boards by keyword.

#### Usage

```bash
aux4 pinterest search boards <query> [--pageSize <n>] [--bookmark <token>] [--tokenFile <path>]
```

--pageSize    Number of results to return (default: 25, max: 100)
--bookmark    Pagination bookmark from previous response
--tokenFile   Custom token file path

#### Example

```bash
aux4 pinterest search boards "travel"
```

```text
{"items":[{"id":"456","name":"Travel Ideas"}],"bookmark":"Pz9..."}
```
