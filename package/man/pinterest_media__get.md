#### Description

The `get` command retrieves the status of a specific media upload by its ID.

#### Usage

```bash
aux4 pinterest media get <mediaId> [--tokenFile <path>]
```

--tokenFile   Custom token file path

#### Example

```bash
aux4 pinterest media get abc123
```

```text
{"media_id":"abc123","media_type":"video","status":"succeeded"}
```
