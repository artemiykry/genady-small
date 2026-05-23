# edit_incident_timeline_entry

Modify an existing timeline entry.

## Input
- `incident`
- `entry_index: int`
- `text: markdown`

## Output
- updated `Incident`

## Side effects
- `incident.timeline[entry_index].text ← text`

## Preconditions
- incident exists
- `entry_index` is a valid offset into `incident.timeline`
