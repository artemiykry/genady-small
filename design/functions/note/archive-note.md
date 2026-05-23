# archive_note

Soft-delete a note.

## Input
- `note`

## Output
- updated `Note`

## Side effects
- `note.archived ← true`
- note becomes read-only

## Preconditions
- note exists
- note is not already archived
