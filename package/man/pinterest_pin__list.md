#### Description

The `list` command retrieves the authenticated user's pins.

#### Usage

```bash
aux4 pinterest pin list [--pageSize <n>] [--apiUrl <url>]
```

--pageSize   Number of pins to return (default: 25, max: 100)
--apiUrl     Pinterest API base URL (default: https://api.pinterest.com)

#### Example

```bash
aux4 pinterest pin list --pageSize 5
```

```text
{"items":[{"id":"123","title":"My Pin"}],"bookmark":"Pz9..."}
```
