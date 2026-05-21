# Incident

A structured record of something going wrong — an outage, a security event, a botched release, a dropped ball.

## Identity
- `id` — UUID.

## Attributes
- **id** `UUID`
- **title** `string`
- **status** `enum(open, postmortem, closed)`
- **started_at** `timestamp`
- **resolved_at** `timestamp?`
- **owner** `→ Person`
- **owner_team** `→ Team`
- **timeline** `TimelineEntry[]` — each `{timestamp, author, text}`; entries can be edited or deleted
- **action_items** `→ Task[]`
- **postmortem** `→ Document?`

## Invariants
- `title` is non-empty.
- `started_at` ≤ `resolved_at` when both are set.
- `resolved_at` is set when `status` is `postmortem` or `closed`.
- A `closed` incident has a `postmortem`.

## Operations
- **create** — capture lightly the moment something breaks.
- **append_timeline_entry / edit_timeline_entry / delete_timeline_entry**.
- **transition** — `open → postmortem → closed`.
- **assign_owner / assign_owner_team**.
- **spawn_action_item** — create a linked [task](tasks.md).
- **draft_postmortem** — create the linked [document](documents.md).

## Relationships
- **→ Person** (1, `owner`)
- **→ Team** (1, `owner_team`)
- **→ Task** (N, `action_items`)
- **→ Document** (0..1, `postmortem`)
- **→ any Entity** (N, via links)
- **← any Entity** (N, backlinks)
