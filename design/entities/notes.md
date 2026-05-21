# Note

A lightweight, low-friction capture artifact — the default home for thoughts whose place is not yet decided.

## Identity
- `id` — UUID.

## Attributes
- **id** `UUID`
- **title** `string?` — derived from first line if blank
- **body** `markdown`
- **created_at** `timestamp`
- **updated_at** `timestamp`
- **archived** `bool`

## Invariants
- `body` is non-empty OR `title` is non-empty.
- An archived note is read-only.

## Operations
- **create** — opens blank in editor; no required fields.
- **edit** — update `title` / `body`.
- **promote** — convert to [task](tasks.md), [document](documents.md), or attach to a [meeting](meetings.md) / [person](people.md); preserves backlinks.
- **archive / restore** — soft-delete and recover.
- **mention** — embed `@person` or `[[entity]]`.

## Relationships
- **→ any Entity** (N, via mentions and links)
- **← any Entity** (N, backlinks)
