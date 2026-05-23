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
