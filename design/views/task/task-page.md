# TaskPage

A single task in detail.

- **Purpose** — see and update one task's full context.
- **Shows** — title, body, status, priority, dates, assignee, parent chain, subtasks, recurrence.
- **Actions** — `update_task`, `transition_task`, `nest_task`, `unnest_task`, `assign_task`, `snooze_task`, `archive_task`, `promote_task_to_document`.
- **States**
  - *active* — non-archived; full editing.
  - *done* — completed; visible but interactions limited to revert / archive.
  - *archived* — read-only.
- **Composed of** — `DocumentEditor` (body), subtask list, `BacklinksPanel`.
