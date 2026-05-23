# Meeting

A note anchored to a calendar event, where what was discussed, decided, and what to do next is captured.

## Identity
- `id` — UUID.

## Attributes
- **id** `UUID`
- **title** `string`
- **event** `→ Event?` — anchoring calendar event; absent for ad-hoc meetings
- **series** `→ MeetingSeries?` — for recurring events
- **attendees** `→ Person[]` — pulled from `event`, editable for ad-hoc
- **agenda** `markdown`
- **notes** `markdown`
- **decisions** `string[]` — explicit, marked, surfaced in search
- **action_items** `ActionItem[]` — each `{text, assignee → Person?, due_date date?, promoted → Task?}`
- **starts_at** `timestamp`
- **ends_at** `timestamp`

## Invariants
- A meeting is anchored to at most one `event`.
- Attendees are unique per meeting.
- `starts_at` < `ends_at`.
