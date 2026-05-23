# archive_task

Soft-delete a task.

## Input
- `task`

## Output
- updated `Task`

## Side effects
- `task.archived ← true`

## Preconditions
- task exists
- task not already archived
