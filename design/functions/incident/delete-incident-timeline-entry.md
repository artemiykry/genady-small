# delete_incident_timeline_entry

Remove a timeline entry from an incident.

## Input
- `incident`
- `entry_index: int`

## Output
- updated `Incident`

## Side effects
- entry removed from `incident.timeline`

## Preconditions
- incident exists
- `entry_index` is a valid offset into `incident.timeline`
