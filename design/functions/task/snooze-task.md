# snooze_task

Defer a task by pushing its scheduled time forward.

## Input
- `task`
- `until: datetime`

## Output
- updated `Task`

## Side effects
- `task.scheduled_at ← until`

## Preconditions
- task exists
- task not archived
- `until` is in the future
