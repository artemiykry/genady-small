# create_document

Make a fresh document.

## Input
- `title: string`
- `body: markdown?`

## Output
- `Document`

## Side effects
- new `Document` persisted
- `created_at = updated_at = now`
- initial entry appended to `versions`

## Preconditions
- `title` non-empty
