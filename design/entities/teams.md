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

## Invariants
- `name` is non-empty.
- A team cannot be its own ancestor (hierarchy is acyclic).
- A person may belong to multiple teams.

## Operations
- **create** — new team.
- **rename** — set `name`.
- **add_member / remove_member** — manage `members`.
- **reparent** — set or clear `parent`.

## Relationships
- **→ Person** (0..1, `manager`)
- **→ Person** (N, `members`)
- **→ Team** (0..1, `parent`)
- **← Team** (N, sub-teams — derived from `parent`)
