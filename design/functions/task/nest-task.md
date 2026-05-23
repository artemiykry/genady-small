# nest_task

Set a task's parent.

## Input
- `task`
- `parent: Task`

## Output
- updated `Task`

## Side effects
- `task.parent ← parent`

## Preconditions
- both tasks exist
- `parent ≠ task`
- assigning `parent` does not create a cycle in the ancestry chain
