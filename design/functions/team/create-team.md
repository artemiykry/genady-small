# create_team

Add a team.

## Input
- `name: string`
- `description: markdown?`
- `parent: Team?`
- `manager: Person?`

## Output
- new `Team`

## Side effects
- new `Team` persisted with empty `members`

## Preconditions
- `name` non-empty
- if `parent` provided, no cycle introduced
