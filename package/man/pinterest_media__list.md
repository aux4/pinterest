#### Description

The `list` command retrieves all registered media uploads for the authenticated user.

#### Usage

```bash
aux4 pinterest media list [--pageSize <n>]
```

--pageSize    Number of uploads to return (default: 25, max: 100)

#### Example

```bash
aux4 pinterest media list
```

```text
{"items":[{"media_id":"abc123","media_type":"video","status":"succeeded"}]}
```
