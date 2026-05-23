# update_task

Edit task attributes.

## Input
- `task`
- any subset of editable attributes (title, body, priority, dates, scheduled_at, assignee, recurrence)

## Output
- updated `Task`

## Side effects
- provided attributes updated
- `updated_at = now`

## Preconditions
- task exists
- task not archived
- attribute invariants hold post-update (`start_date ≤ due_date`, etc.)
