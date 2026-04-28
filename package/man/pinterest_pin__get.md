#### Description

The `get` command retrieves a single pin by its ID.

#### Usage

```bash
aux4 pinterest pin get <pinId> [--tokenFile <path>]
```

--tokenFile   Custom token file path

#### Example

```bash
aux4 pinterest pin get 123456789
```

```text
{"id":"123456789","title":"My Pin","description":"A pin","board_id":"987654"}
```
