#### Description

The `update` command updates an existing pin. Only the fields included in `--body` are modified.

#### Usage

```bash
aux4 pinterest pin update <pinId> --body <json> [--tokenFile <path>]
```

--body        Pin fields to update as JSON (title, description, link, alt_text)
--tokenFile   Custom token file path

#### Example

```bash
aux4 pinterest pin update 123456789 --body '{"title":"Updated Title","description":"New description"}'
```

```text
{"id":"123456789","title":"Updated Title","description":"New description"}
```
