#### Description

The `pins` command lists all pins within a specific board section.

#### Usage

```bash
aux4 pinterest board section pins --boardId <boardId> <sectionId> [--pageSize <n>] [--bookmark <token>] [--tokenFile <path>]
```

--boardId     Board ID
--pageSize    Number of pins to return (default: 25, max: 100)
--bookmark    Pagination bookmark from previous response
--tokenFile   Custom token file path

#### Example

```bash
aux4 pinterest board section pins --boardId 123456 789012
```

```text
{"items":[{"id":"111","title":"Pin in Section"}]}
```
