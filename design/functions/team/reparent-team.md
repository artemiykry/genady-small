# reparent_team

Move a team under a new parent, or to the top level.

## Input
- `team`
- `parent: Team?` — `null` to detach

## Output
- updated `Team`

## Side effects
- `team.parent ← parent`

## Preconditions
- team exists
- if `parent` provided, `parent ≠ team` and no cycle introduced
