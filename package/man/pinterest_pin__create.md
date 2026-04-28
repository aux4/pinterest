#### Description

The `create` command creates a new pin on Pinterest. The pin data must be provided as JSON with `--body`, including at minimum a `board_id` and a `media_source`.

#### Usage

```bash
aux4 pinterest pin create --body <json> [--tokenFile <path>]
```

--body        Pin data as JSON (title, description, board_id, media_source, link, alt_text)
--tokenFile   Custom token file path

#### Example

```bash
aux4 pinterest pin create --body '{"title":"Summer Recipe","description":"Delicious pasta","board_id":"123456","media_source":{"source_type":"image_url","url":"https://example.com/pasta.jpg"}}'
```

```text
{"id":"789012","title":"Summer Recipe","board_id":"123456"}
```
