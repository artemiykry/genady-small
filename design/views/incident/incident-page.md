# IncidentPage

Single incident with its full record.

- **Purpose** — capture, resolve, and document one incident in one place.
- **Shows** — title, status, owner, owner_team, started_at, resolved_at, timeline, action items, postmortem link.
- **Actions** — `edit_incident`, `transition_incident`, `append_incident_timeline_entry`, `edit_incident_timeline_entry`, `delete_incident_timeline_entry`, `assign_incident_owner`, `assign_incident_owner_team`, `spawn_incident_action_item`, `draft_incident_postmortem`; open postmortem in `DocumentPage`.
- **States**
  - *active* — status `open` or `postmortem`; timeline editable.
  - *closed* — read-only timeline; transitions disabled.
- **Composed of** — incident-timeline list, action-item list, `BacklinksPanel`.
