#### Description

The `section` command group manages board sections. Sections let you organize pins within a board.

Available subcommands: `create`, `list`, `update`, `delete`, `pins`.

#### Usage

```bash
aux4 pinterest board section <subcommand> [options]
```

#### Example

```bash
aux4 pinterest board section list 123456
aux4 pinterest board section create 123456 --body '{"title":"Favorites"}'
```
