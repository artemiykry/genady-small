# create_meeting

Create a meeting, with or without a calendar event.

## Input
- `title: string`
- `event: Event?`
- `starts_at: timestamp`
- `ends_at: timestamp`

## Output
- new `Meeting`

## Side effects
- new `Meeting` persisted
- if `event` provided, `attendees` pulled from event

## Preconditions
- `title` non-empty
- `starts_at` < `ends_at`
