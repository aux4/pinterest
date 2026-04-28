#### Description

The `upload` command registers a media upload with Pinterest. After registration, use the returned upload URL to upload the actual media file, then reference the media ID when creating a pin.

#### Usage

```bash
aux4 pinterest media upload --body <json> [--tokenFile <path>]
```

--body        Media upload data as JSON (media_type: "video")
--tokenFile   Custom token file path

#### Example

```bash
aux4 pinterest media upload --body '{"media_type":"video"}'
```

```text
{"media_id":"abc123","media_type":"video","upload_url":"https://...","upload_parameters":{}}
```
