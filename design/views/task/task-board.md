# TaskBoard

Kanban-style task view grouped by status.

- **Purpose** — see flow across status columns; drag to transition.
- **Shows** — columns: `todo`, `doing`, `blocked`, `done`; tasks as cards filtered by current criteria.
- **Actions** — `transition_task` via drag-drop; `assign_task` via card actions; open `TaskPage`.
- **States**
  - *active* — non-archived tasks.
  - *filtered* — narrowed by assignee, parent, or other criteria.
- **Composed of** — column header, task card.
