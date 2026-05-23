# create_task

Add a task.

## Input
- `title: string`
- `body: markdown?`
- `assignee: Person?`
- `due_date: date?`
- `start_date: date?`
- `scheduled_at: datetime?`
- `parent: Task?`
- `recurrence: RecurrenceRule?`

## Output
- new `Task`

## Side effects
- new `Task` persisted with `status = todo`, `priority = none`, `archived = false`

## Preconditions
- `title` non-empty
- if `parent` provided, no cycle introduced
- if `start_date` and `due_date` both provided, `start_date ≤ due_date`
