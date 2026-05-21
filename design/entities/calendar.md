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

## Invariants
- `starts_at` < `ends_at`.
- Source-owned fields reflect external state on each sync; local fields persist across re-sync.
- The app never writes to the source.

## Operations
- **annotate** — edit `annotations` (local-only).
- **link** — attach to any local entity.
- **attach_meeting** — open or auto-create a [meeting](meetings.md) for the event.
- **resolve_attendee** — map a source attendee to a local [person](people.md).

## Relationships
- **→ Person** (N, `attendees`)
- **→ Meeting** (0..1)
- **→ any Entity** (N, `links`)
- **← any Entity** (N, backlinks)
