# annotate_event

Edit the local annotations on an event.

## Input
- `event`
- `annotations: markdown`

## Output
- updated `Event`

## Side effects
- `event.annotations ← annotations`
- never written to the source calendar

## Preconditions
- event exists
