#### Description

The `update` command updates an existing board section's title.

#### Usage

```bash
aux4 pinterest board section update --boardId <boardId> <sectionId> --body <json> [--tokenFile <path>]
```

--boardId     Board ID
--body        Section fields to update as JSON (title)
--tokenFile   Custom token file path

#### Example

```bash
aux4 pinterest board section update --boardId 123456 789012 --body '{"title":"Top Picks"}'
```
