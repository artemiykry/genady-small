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
