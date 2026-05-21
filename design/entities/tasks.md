# Tasks

A task is a unit of intent — something you want done, by you or someone else.

## Shape

Each task has:
- **Title** — short, the thing
- **Body** — optional notes, context, links
- **Status** — `todo`, `doing`, `done`, `blocked`, `cancelled`
- **Priority** — none / low / medium / high / urgent
- **Dates** — start, due, scheduled (when you plan to work on it)
- **Assignee** — a [person](people.md), often yourself
- **Links** — to docs, notes, meetings, incidents, other tasks, people

## Nesting

Tasks nest arbitrarily deep. A subtask is just a task whose parent is another task. A task with subtasks can:
- Roll up progress (e.g. "3 of 7 done")
- Be completed independently of its children (with a warning)

There is no distinction between "project," "epic," "story," "task." All are tasks. Depth is up to the user.

## Recurrence

A task can recur on a schedule (daily, weekly, custom). Completing the current instance generates the next one.

## Views

Two ways to look at tasks. Both share the same filter (`person:@alex AND status:todo` works in either) and switch with a keystroke.

### Outline-table

A tree with columns. Tasks nest visually with expand / collapse; each row shows the fields you care about — status, priority, due date, assignee. Sort, filter, group, bulk-edit. The default. Equally good for inbox triage, daily planning, and breaking down a project.

### Gantt

A horizontal timeline. Each task is a bar from start to due; nesting collapses into parent bars; dependencies show as arrows. For seeing slack, conflicts, and shape over weeks.

### Saved views

A view is a filter + a shape (outline-table or gantt) + visible columns + grouping + sort. Name one and pin it to the sidebar — "Today," "This Week," "Blocked," "Waiting on Alex" are all just saved views.

## What you can do

- Create a task from anywhere — global hotkey, agent, inside a note, from a calendar event.
- Drag to reorder, indent, outdent.
- Convert: a note becomes a task; a task becomes a doc; a meeting action item becomes a task.
- Snooze, defer, archive.
- Bulk edit across a view.

## What lives elsewhere

- *Who* a task belongs to → [people](people.md)
