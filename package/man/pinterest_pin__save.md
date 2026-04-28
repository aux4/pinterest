#### Description

The `save` command saves an existing pin to a board. You can optionally specify a board section.

#### Usage

```bash
aux4 pinterest pin save <pinId> --body <json>
```

--body        Save data as JSON (board_id, board_section_id)

#### Example

```bash
aux4 pinterest pin save 123456789 --body '{"board_id":"987654"}'
```
