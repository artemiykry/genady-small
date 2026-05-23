# Plan the week

At the start of the week, decide what gets done and when.

## Goal
Each task the user expects to work on has a `scheduled_at` within the week and a clear priority.

## Trigger
User opens `TaskList` on Monday morning.

## Steps
1. **View:** `TaskList` in *all_active* state.
2. User filters by no-`scheduled_at` and `status = todo`.
3. For each candidate, user selects rows and applies bulk priority via:
4. **Function:** `bulk_edit_tasks(tasks, { priority })`.
5. For tasks worth doing this week, user picks a slot:
6. **Function:** `update_task(task, { scheduled_at })`.
7. For tasks not for this week, user defers:
8. **Function:** `snooze_task(task, until)`.
9. **View:** switch to `TaskBoard` to validate flow across status columns.

## Postconditions
- Every task expected this week has `scheduled_at` set.
- Every deferred task has been snoozed to a specific future date.
- Priority distribution looks intentional, not accidental.

## Failure paths
- User loses focus mid-triage → state preserved; list filters persist.
