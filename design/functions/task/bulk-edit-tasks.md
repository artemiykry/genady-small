# bulk_edit_tasks

Apply a single update across many tasks.

## Input
- `tasks: Task[]`
- `update` — same shape as `update_task` input

## Output
- updated `Task[]`

## Side effects
- `update_task` applied to each task transactionally — all succeed or all roll back

## Preconditions
- every task exists and is not archived
- per-task application would satisfy `update_task` preconditions
