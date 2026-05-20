# Skills

Skills are named, reusable capabilities the agent reaches for. Each skill packages a competence — *"weekly review,"* *"draft a client update,"* *"extract action items from a transcript,"* *"turn this meeting series into a one-pager."*

## What a skill is

- **Name** — short, invocable (`/weekly-review`)
- **Description** — what it does, when to use it
- **Instructions** — the prompt / procedure the agent follows
- **Allowed surface** — which entities, files, [shell](shell.md), or [MCP](mcp.md) tools the skill can touch
- **Trigger** — manual, implicit, or scheduled

## Where they come from

- **Built-in** — ship with the app for the common patterns: recap a meeting, draft an update, extract action items, summarize a series, plan a week, prepare a 1:1.
- **Custom** — you author your own as plain files. Edit them like any document; they live alongside your workspace.
- **Imported** — bring in a skill someone else wrote.

## Library

A searchable list of all skills. Pin the ones you reach for often. Skills surface by name and description, not by category.

## Invocation

- **Direct** — type `/skill-name` in chat, or pick from the library.
- **Implicit** — the agent picks a skill when the conversation matches its description, names which one it chose, and you can swap.
- **Inline** — invoke from inside a specific entity (task, doc, meeting, person) with that entity pre-loaded as context.
- **Scheduled** — some skills run on a cadence (e.g. *"weekly review"* fires every Friday).

## What lives elsewhere

- Persistent context the skill draws on → [memory](memory.md)
- What a skill is allowed to do without asking → [approval workflow](approval.md)
