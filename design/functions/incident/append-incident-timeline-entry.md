# append_incident_timeline_entry

Add a new entry to an incident timeline.

## Input
- `incident`
- `text: markdown`
- `timestamp: timestamp?` — defaults to now

## Output
- updated `Incident`

## Side effects
- new `TimelineEntry{timestamp, author, text}` appended to `incident.timeline`

## Preconditions
- incident exists
- `text` non-empty
