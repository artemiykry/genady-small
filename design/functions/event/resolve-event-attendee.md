# resolve_event_attendee

Map a source-calendar attendee to a local person.

## Input
- `event`
- `external_attendee: string` — identifier in the source (e.g. email)
- `person`

## Output
- updated `Event`

## Side effects
- attendee entry resolves to `person` in the event's local attendee mapping

## Preconditions
- event exists
- person exists
- `external_attendee` is present on `event`
