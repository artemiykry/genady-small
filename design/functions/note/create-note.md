# create_note

Create a blank note for capture.

## Input
- `body: markdown?`
- `title: string?`

## Output
- new `Note`

## Side effects
- new `Note` persisted with `archived = false`, `created_at = updated_at = now`

## Preconditions
- none — notes can be created blank and filled in via `edit_note`
