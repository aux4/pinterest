#### Description

The `pins` command lists all pins on a specific board.

#### Usage

```bash
aux4 pinterest board pins <boardId> [--pageSize <n>] [--bookmark <token>] [--tokenFile <path>]
```

--pageSize    Number of pins to return (default: 25, max: 100)
--bookmark    Pagination bookmark from previous response
--tokenFile   Custom token file path

#### Example

```bash
aux4 pinterest board pins 123456 --pageSize 10
```

```text
{"items":[{"id":"789","title":"My Pin"}],"bookmark":"Pz9..."}
```
