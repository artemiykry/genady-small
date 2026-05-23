# PeopleDirectory

All people known to the system.

- **Purpose** — find a person; review the roster.
- **Shows** — person rows with name, role, team, status.
- **Actions** — `create_person`; open `PersonPage`; filter active / former; search by name or alias.
- **States**
  - *active* — only active.
  - *former* — only former.
  - *all* — both.
- **Composed of** — person row.
