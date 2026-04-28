#### Description

The `create` command creates a new board on Pinterest.

#### Usage

```bash
aux4 pinterest board create --body <json> [--tokenFile <path>]
```

--body        Board data as JSON (name, description, privacy)
--tokenFile   Custom token file path

#### Example

```bash
aux4 pinterest board create --body '{"name":"Travel Ideas","description":"Places to visit","privacy":"PUBLIC"}'
```

```text
{"id":"123456","name":"Travel Ideas","privacy":"PUBLIC"}
```
