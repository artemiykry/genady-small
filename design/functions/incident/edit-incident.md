# edit_incident

Update an incident's mutable attributes (excluding status, owner, owner_team, timeline, action_items, postmortem — those have their own functions).

## Input
- `incident`
- any subset of: `title`, `started_at`, `resolved_at`

## Output
- updated `Incident`

## Side effects
- provided attributes updated

## Preconditions
- incident exists
- if `title` provided, non-empty
- if both `started_at` and `resolved_at` set after update, `started_at ≤ resolved_at`
