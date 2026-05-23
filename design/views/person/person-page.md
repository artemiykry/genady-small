# PersonPage

A single person with everything related.

- **Purpose** — orient on a colleague before a meeting; capture longer-term context.
- **Shows** — name, aliases, role, teams, contact, status, brief document, attended meetings, assigned tasks.
- **Actions** — `update_person`, `merge_people`, `set_person_status`; edit brief (opens `DocumentPage`); open any related entity.
- **States**
  - *active* — full editing.
  - *former* — soft read-only; merge and history still available.
- **Composed of** — `DocumentEditor` (brief), related-entity lists, `BacklinksPanel`.
