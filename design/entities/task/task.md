# Task

A unit of intent — something you want done, by you or someone else.

## Identity
- `id` — UUID, opaque, stable across renames.

## Attributes
- **id** `UUID`
- **title** `string`
- **body** `markdown?`
- **status** `enum(todo, doing, done, blocked, cancelled)`
- **priority** `enum(none, low, medium, high, urgent)`
- **start_date** `date?`
- **due_date** `date?`
- **scheduled_at** `datetime?`
- **assignee** `→ Person?`
- **parent** `→ Task?`
- **subtasks** `→ Task[]` — derived from `Task.parent`
- **recurrence** `RecurrenceRule?` — daily, weekly, or custom
- **created_at** `timestamp`
- **updated_at** `timestamp`
- **completed_at** `timestamp?`
- **archived** `bool`

## Invariants
- `title` is non-empty.
- A task cannot be its own ancestor (nesting is acyclic).
- `completed_at` is set iff `status` is `done`.
- `start_date` ≤ `due_date` when both are set.
- Completing a recurring instance generates the next instance.
