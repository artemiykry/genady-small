# unnest_task

Clear a task's parent.

## Input
- `task`

## Output
- updated `Task`

## Side effects
- `task.parent ← null`

## Preconditions
- task exists
- `task.parent` was set
