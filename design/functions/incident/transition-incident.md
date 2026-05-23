# transition_incident

Move an incident through its lifecycle.

## Input
- `incident`
- `next_status: enum(open, postmortem, closed)`

## Output
- updated `Incident`

## Side effects
- `incident.status ← next_status`
- if `next_status ∈ {postmortem, closed}` and `resolved_at` is unset, `resolved_at = now`

## Preconditions
- incident exists
- valid transition: `open → postmortem`, `open → closed`, `postmortem → closed`
- `next_status = closed` requires `incident.postmortem` to be set
