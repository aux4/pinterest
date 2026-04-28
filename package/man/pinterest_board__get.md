#### Description

The `get` command retrieves a single board by its ID.

#### Usage

```bash
aux4 pinterest board get <boardId> [--tokenFile <path>]
```

--tokenFile   Custom token file path

#### Example

```bash
aux4 pinterest board get 123456
```

```text
{"id":"123456","name":"Travel Ideas","description":"Places to visit","privacy":"PUBLIC"}
```
