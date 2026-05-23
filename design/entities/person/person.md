# Person

A first-class entity for a colleague — so they can be referenced, queried, and reasoned about, not just typed as a string.

## Identity
- `id` — UUID.

## Attributes
- **id** `UUID`
- **name** `string`
- **aliases** `string[]`
- **role** `string?` — free text (title, function)
- **teams** `→ Team[]`
- **contact** `map<string, string>` — open-ended identifiers (`email`, `slack`, `github`, `phone`, …)
- **status** `enum(active, former)`
- **brief** `→ Document` — single doc attached to the person; topics, longer-term things, feedback, follow-ups
- **attended_meetings** `→ Meeting[]` — derived from `Meeting.attendees`
- **assigned_tasks** `→ Task[]` — derived from `Task.assignee`

## Invariants
- `name` is non-empty.
- Aliases are unique within a person.
- Every person has exactly one `brief` document (auto-created on first need).
