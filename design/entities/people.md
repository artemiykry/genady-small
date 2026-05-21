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

## Invariants
- `name` is non-empty.
- Aliases are unique within a person.
- Every person has exactly one `brief` document (auto-created on first need).

## Operations
- **create** — manually, or by approving a calendar-attendee auto-suggestion.
- **update** — edit any attribute.
- **merge** — combine duplicate persons; backlinks rewrite.
- **set_status** — `active` / `former`.

## Relationships
- **→ Team** (N, `teams`)
- **→ Document** (1, `brief`)
- **→ Meeting** (N, attendance — derived)
- **→ Task** (N, assignee — derived)
- **← any Entity** (N, backlinks)
