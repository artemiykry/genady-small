# TaskList

Flat list of tasks with filters.

- **Purpose** — work through pending intent.
- **Shows** — task rows with title, status, priority, due_date, assignee, parent context.
- **Actions** — `create_task`; per row: `transition_task`, `assign_task`, `snooze_task`, `archive_task`; across selection: `bulk_edit_tasks`.
- **States**
  - *today* — scheduled or due today.
  - *overdue* — past `due_date` and not done.
  - *all_active* — non-archived.
  - *archived* — archived only.
- **Composed of** — task row, filter bar, selection toolbar.
