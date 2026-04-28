#### Description

The `delete` command permanently deletes a board section. Pins in the section are moved to the board's unsectioned area. You will be asked for confirmation.

#### Usage

```bash
aux4 pinterest board section delete --boardId <boardId> <sectionId>
```

--boardId     Board ID

#### Example

```bash
aux4 pinterest board section delete --boardId 123456 789012
```

```text
Are you sure you want to delete section 789012? (y/n)
```
