# Task

A unit of intent — something you want done, by you or someone else.

## Identity
- `id` — UUID, opaque, stable across renames.

## Attributes
- **id** `UUID`
- **title** `string`
- **body** `markdown?`
- **status** `enum(todo, doing, done, blocked, cancelled)`
- **priority** `enum(none, low, medium, high, urgent)`
- **start_date** `date?`
- **due_date** `date?`
- **scheduled_at** `datetime?`
- **assignee** `→ Person?`
- **parent** `→ Task?`
- **recurrence** `RecurrenceRule?` — daily, weekly, or custom
- **created_at** `timestamp`
- **updated_at** `timestamp`
- **completed_at** `timestamp?`
- **archived** `bool`

## Invariants
- `title` is non-empty.
- A task cannot be its own ancestor (nesting is acyclic).
- `completed_at` is set iff `status` is `done`.
- `start_date` ≤ `due_date` when both are set.
- Completing a recurring instance generates the next instance.

## Operations
- **create** — from anywhere (global hotkey, agent, inside a note, from a calendar event).
- **update** — edit any attribute.
- **transition** — change `status`.
- **nest / unnest** — set or clear `parent`.
- **assign** — set `assignee`.
- **snooze / defer** — push `scheduled_at` forward.
- **archive** — soft-delete; recoverable.
- **convert** — promote into a [document](documents.md).
- **bulk_edit** — apply updates across a filtered set.

## Relationships
- **→ Person** (0..1, `assignee`)
- **→ Task** (0..1, `parent`)
- **← Task** (N, subtasks — derived from `parent`)
- **→ any Entity** (N, via links)
- **← any Entity** (N, backlinks)
