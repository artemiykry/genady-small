# link_event

Attach an event to a local entity.

## Input
- `event`
- `target: any Entity`

## Output
- updated `Event`

## Side effects
- `target` appended to `event.links`
- `target` gains a backlink to `event`

## Preconditions
- event exists
- target exists
