# edit_document

Replace the body; previous body is preserved in history.

## Input
- `document`
- `new_body: markdown`

## Output
- updated `Document`

## Side effects
- current `body` appended to `versions` with prior `updated_at`
- `body ← new_body`
- `updated_at = now`
- backlinks recomputed

## Preconditions
- document exists
