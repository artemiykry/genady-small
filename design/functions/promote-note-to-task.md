# promote_note_to_task

Convert a note into a tracked task.

## Input
- `note`

## Output
- new `Task`

## Side effects
- new `Task` created via `create_task` with `title` from note title or first line and `body` from note body
- backlinks targeting the note are rewritten to target the task
- original note is archived

## Preconditions
- note exists
- note is not archived
