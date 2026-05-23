# detach_meeting_from_event

Sever the link between a meeting and its calendar event; the meeting becomes ad-hoc.

## Input
- `meeting`

## Output
- updated `Meeting`

## Side effects
- `meeting.event ← null`
- attendees become locally owned (no longer pulled from event)

## Preconditions
- meeting exists
- `meeting.event` is set
