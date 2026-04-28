#### Description

The `create` command creates a new board on Pinterest.

#### Usage

```bash
aux4 pinterest board create --body <json>
```

--body        Board data as JSON (name, description, privacy)

#### Example

```bash
aux4 pinterest board create --body '{"name":"Travel Ideas","description":"Places to visit","privacy":"PUBLIC"}'
```

```text
{"id":"123456","name":"Travel Ideas","privacy":"PUBLIC"}
```
