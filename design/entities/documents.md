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

## Operations
- **create** — fresh document.
- **edit** — append a new version.
- **restore_version** — promote a prior version to current.
- **embed** — link to or inline another entity.
- **mention** — `@person` or `[[entity]]`.
- **promote_from_note** — convert an existing [note](notes.md); content moves, backlinks update.

## Relationships
- **→ any Entity** (N, via embeds, mentions, links)
- **← any Entity** (N, backlinks)
