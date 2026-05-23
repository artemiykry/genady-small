# Team

A container for [people](people.md), nested arbitrarily — for mapping the organization, modeling reporting lines, or grouping collaborators.

## Identity
- `id` — UUID.

## Attributes
- **id** `UUID`
- **name** `string`
- **description** `markdown?`
- **manager** `→ Person?`
- **members** `→ Person[]`
- **parent** `→ Team?`
- **subteams** `→ Team[]` — derived from `Team.parent`

## Invariants
- `name` is non-empty.
- A team cannot be its own ancestor (hierarchy is acyclic).
- A person may belong to multiple teams.
