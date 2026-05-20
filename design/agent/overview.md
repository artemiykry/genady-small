# Agent

The agent is a chat companion that can read and act on your workspace — your tasks, calendar, meetings, incidents, notes, documents, people, teams, and the files tree. It is not a separate "AI feature"; it is a participant in the same graph you live in.

## What it can do

- **Find** — *"what did I promise Alex last month?"* — searches across notes, meetings, tasks, documents, incidents, and file contents.
- **Summarize** — recap a meeting series, distill a long document, surface what changed this week.
- **Capture** — turn dictation or rambling chat into a structured task, note, or doc.
- **Plan** — propose a schedule, break a goal into subtasks, suggest who to involve.
- **Maintain** — archive stale notes, link orphan items, fix inconsistencies you describe.
- **Build views** — *"give me a view of everything blocked"* produces a saved task view.
- **Schedule** — create events, draft a meeting agenda, propose times.
- **Edit files** — open, read, modify, create, move, and delete files in the [files](../entities/files.md) tree.

## How it behaves

- **Shows its work** — every action it takes (create, edit, link) is visible and reversible.
- **Asks when uncertain** — it surfaces ambiguity instead of guessing.
- **Has context** — it knows what you're currently looking at, what you've linked, who you've met with.
- **Has memory** — see [memory](memory.md); patterns, preferences, recurring people and projects persist across sessions.
- **Stays within bounds** — every action runs under the [approval workflow](approval.md); the agent never sends externally or deletes without explicit consent.

## Where it lives

- A dedicated chat pane, always one shortcut away.
- Inline: invoke from inside any note, task, or doc — the current entity is its context by default.
- Proactive (opt-in): suggestions at the start of the day, before a meeting, on a stalled task.

## How it's built up

- [Skills](skills.md) — named, reusable capabilities, built-in or user-authored
- [Memory](memory.md) — persistent context across sessions
- [Shell](shell.md) — execute commands on your machine
- [Approval workflow](approval.md) — what runs freely vs. what waits for you
- [MCP](mcp.md) — connect external tools and data sources
