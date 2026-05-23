# transition_task

Change a task's status.

## Input
- `task`
- `next_status: enum(todo, doing, done, blocked, cancelled)`

## Output
- updated `Task`

## Side effects
- `task.status ← next_status`
- if `next_status = done`, set `completed_at = now`
- if leaving `done`, clear `completed_at`
- if `task.recurrence` is set and `next_status = done`, generate the next recurring instance via `create_task`

## Preconditions
- task exists
- task not archived
