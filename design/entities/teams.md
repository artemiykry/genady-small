# Teams

Teams are containers for [people](people.md), nested arbitrarily. Useful for mapping your organization, modeling reporting lines, or grouping collaborators for views and filters.

## Shape

Each team has:
- **Name** — "Platform," "Eng / Infra," "Customer Success / EMEA"
- **Manager** — a [person](people.md)
- **Members** — people in this team directly
- **Parent team** — for nesting (e.g. "Eng / Infra" lives inside "Eng")
- **Sub-teams** — automatic from children

## Hierarchy

Teams nest — a team can contain teams which contain teams. There is no distinction between "department," "team," "squad" — depth is up to you.

A person can belong to multiple teams (matrixed, dotted-line, working-group), and rolls up to all ancestors automatically.

## What you can do

- Create teams, drag people in, rename, nest, reparent.
- Open a team page — see its members, sub-teams, linked tasks and docs.
- `@team-name` mentions anywhere.
- Filter task views by team — *"open tasks owned by anyone in Platform."*
- Roll up — at a parent team, see members and activity aggregated across descendants.

## What lives elsewhere

- Per-person profile, one-on-ones, plans → on each [person's](people.md) page
