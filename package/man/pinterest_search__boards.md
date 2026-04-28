#### Description

The `boards` command searches the authenticated user's boards by keyword.

#### Usage

```bash
aux4 pinterest search boards <query> [--pageSize <n>]
```

--pageSize    Number of results to return (default: 25, max: 100)

#### Example

```bash
aux4 pinterest search boards "travel"
```

```text
{"items":[{"id":"456","name":"Travel Ideas"}],"bookmark":"Pz9..."}
```
