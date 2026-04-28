#### Description

The `update` command updates an existing board. Only the fields included in `--body` are modified.

#### Usage

```bash
aux4 pinterest board update <boardId> --body <json>
```

--body        Board fields to update as JSON (name, description, privacy)

#### Example

```bash
aux4 pinterest board update 123456 --body '{"name":"Updated Board Name"}'
```
