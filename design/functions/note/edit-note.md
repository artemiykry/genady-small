# edit_note

Update a note's title or body.

## Input
- `note`
- `title: string?`
- `body: markdown?`

## Output
- updated `Note`

## Side effects
- provided fields updated
- `updated_at = now`
- backlinks recomputed

## Preconditions
- note exists
- note is not archived
- after update, `body` or `title` is non-empty
