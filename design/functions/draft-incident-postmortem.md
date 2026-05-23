# draft_incident_postmortem

Create the postmortem document linked to an incident.

## Input
- `incident`

## Output
- `Document` (new, or existing if already drafted)

## Side effects
- new `Document` created via `create_document` with title derived from incident
- `incident.postmortem ← document`

## Preconditions
- incident exists
- idempotent — if `incident.postmortem` is already set, returns the existing document
