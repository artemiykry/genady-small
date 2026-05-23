# assign_task

Set or clear a task's assignee.

## Input
- `task`
- `person: Person?` — `null` to unassign

## Output
- updated `Task`

## Side effects
- `task.assignee ← person`

## Preconditions
- task exists
- if `person` provided, person exists and is `active`
