# attach_meeting_to_event

Open or create a meeting anchored to a calendar event.

## Input
- `event`

## Output
- `Meeting`

## Side effects
- if a meeting already exists for `event`, return it
- otherwise create a new `Meeting` with `event ← event`, attendees pulled from event, `starts_at` / `ends_at` copied from event

## Preconditions
- event exists
