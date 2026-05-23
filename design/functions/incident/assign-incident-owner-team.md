# assign_incident_owner_team

Set the team responsible for an incident.

## Input
- `incident`
- `team`

## Output
- updated `Incident`

## Side effects
- `incident.owner_team ← team`

## Preconditions
- incident exists
- team exists
