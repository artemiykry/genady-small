# spawn_incident_action_item

Create a follow-up task linked to an incident.

## Input
- `incident`
- `title: string`
- `assignee: Person?`

## Output
- new `Task`

## Side effects
- new `Task` created via `create_task`
- task appended to `incident.action_items`
- task gains a backlink to the incident

## Preconditions
- incident exists
- `title` non-empty
