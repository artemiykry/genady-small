# add_team_member

Add a person to a team.

## Input
- `team`
- `person`

## Output
- updated `Team`

## Side effects
- `person` appended to `team.members`
- `person.teams` includes `team` (derived)

## Preconditions
- team exists
- person exists
- person not already a member
