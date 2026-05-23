# assign_incident_owner

Set the person responsible for an incident.

## Input
- `incident`
- `person`

## Output
- updated `Incident`

## Side effects
- `incident.owner ← person`

## Preconditions
- incident exists
- person exists and is `active`
