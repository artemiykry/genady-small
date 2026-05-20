# Memory

The agent has persistent memory that survives across chat sessions. Memory keeps the agent coherent — knowing your role, your preferences, your patterns, the people and projects you work with — without you re-explaining each time.

## What goes in memory

- **About you** — your role, focus areas, communication preferences
- **Feedback** — corrections you've given, approaches you've validated
- **Project / team context** — ongoing initiatives, stakeholders, deadlines
- **References** — pointers to where things live (which doc covers what, which top-level task is the rollup)

Memory holds *summaries*, not raw content. Workspace entities are the source of truth; memory points at them and adds context the entities themselves don't carry.

## How memory is written

- The agent decides when to write — usually after surprises, corrections, or repeated patterns.
- You can write directly: *"remember that I don't want auto-generated action items."*
- Each memory is a small note with a clear topic. Compact, editable, deletable.
- The agent shows what it wrote when it writes it; you can correct on the spot.

## How memory is read

- The agent pulls memories relevant to what you're doing now.
- Before acting on a memory's claim, the agent verifies against the current workspace — memory can go stale.
- Stale or contradicted memories get updated or removed automatically.

## What you can do

- Browse the full memory list — it's a regular view, organized by topic.
- Edit any memory directly.
- Lock a memory you never want overwritten.
- Ask the agent to forget something: *"forget that I prefer X."*

## What memory is not

- Not your personal data store — entities live in the workspace, not in memory.
- Not a chat archive — chat history is separate.
- Not a substitute for [documents](../entities/documents.md) — long-form knowledge belongs in docs, not memory.
