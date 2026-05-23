# create_incident

Capture an incident the moment something breaks.

## Input
- `title: string`
- `started_at: timestamp?` — defaults to now

## Output
- new `Incident`

## Side effects
- new `Incident` persisted with `status = open`

## Preconditions
- `title` non-empty
