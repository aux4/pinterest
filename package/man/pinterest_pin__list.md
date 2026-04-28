#### Description

The `list` command retrieves the authenticated user's pins. Results are paginated; use `--bookmark` with the value from the previous response to get the next page.

#### Usage

```bash
aux4 pinterest pin list [--pageSize <n>] [--bookmark <token>] [--tokenFile <path>]
```

--pageSize    Number of pins to return (default: 25, max: 100)
--bookmark    Pagination bookmark from previous response
--tokenFile   Custom token file path

#### Example

```bash
aux4 pinterest pin list --pageSize 5
```

```text
{"items":[{"id":"123","title":"My Pin"}],"bookmark":"Pz9..."}
```
