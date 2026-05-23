# Document

A persistent, structured, authored piece of writing — referenced by other entities far more than the reverse.

## Identity
- `id` — UUID.

## Attributes
- **id** `UUID`
- **title** `string`
- **body** `markdown`
- **created_at** `timestamp`
- **updated_at** `timestamp`
- **versions** `Version[]` — append-only edit history; each `{timestamp, author, body}`

## Invariants
- `title` is non-empty.
- `versions` is append-only.
