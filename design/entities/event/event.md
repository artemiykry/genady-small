# Event

A scheduled occurrence on an external calendar, surfaced inside the app with local annotations and links.

## Identity
- `(source, external_id)` — composite key from the origin calendar.

## Attributes
- **external_id** `string` — id in the source calendar
- **source** `enum(google, caldav, outlook)`
- **title** `string` — source-owned
- **starts_at** `timestamp` — source-owned
- **ends_at** `timestamp` — source-owned
- **attendees** `→ Person[]` — source-owned, mapped to local people
- **annotations** `markdown` — local-only; never sync out
- **links** `→ any Entity[]` — local-only
- **meeting** `→ Meeting?` — derived from `Meeting.event`

## Invariants
- `starts_at` < `ends_at`.
- Source-owned fields reflect external state on each sync; local fields persist across re-sync.
- The app never writes to the source.
