# Run an incident end-to-end

Something is on fire — capture the unfolding event, manage response, write the postmortem, close it out.

## Goal
A complete Incident record: timeline, action items, postmortem document, closed status.

## Trigger
User notices a production issue.

## Steps

### Capture (first 5 minutes)
1. **View:** `QuickCapture` → `/incident` command.
2. **Function:** `create_incident(title)` — status starts `open`.
3. **View:** navigate to `IncidentPage` (state: *active*).
4. **Function:** `assign_incident_owner(incident, person)`, `assign_incident_owner_team(incident, team)`.

### Respond
5. As updates arrive, user appends to the timeline:
6. **Function:** `append_incident_timeline_entry(incident, text)`.
7. Follow-ups become tasks:
8. **Function:** `spawn_incident_action_item(incident, title, assignee)`.

### Resolve
9. Once the immediate fire is out:
10. **Function:** `edit_incident(incident, { resolved_at })` (or set implicitly via transition).
11. **Function:** `transition_incident(incident, postmortem)`.

### Document
12. **Function:** `draft_incident_postmortem(incident)` — creates linked `Document`.
13. **View:** `DocumentPage` opens for the postmortem; user writes it up using `edit_document`.

### Close
14. **Function:** `transition_incident(incident, closed)`.
15. **View:** `IncidentPage` enters *closed* state — read-only timeline.

## Postconditions
- Incident has full timeline, owner, owner_team, action_items, postmortem.
- Status is `closed`; postmortem exists.
- All action items are tracked Tasks with backlinks to the incident.

## Failure paths
- Trying to close without a postmortem → `transition_incident` rejects.
