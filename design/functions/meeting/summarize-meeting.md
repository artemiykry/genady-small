# summarize_meeting

Agent-driven recap of a meeting's notes.

## Input
- `meeting`

## Output
- `markdown` summary

## Side effects
- calls the agent (LLM) to produce a summary
- summary is not persisted; caller decides whether to write it into `notes`

## Preconditions
- meeting exists
- `meeting.notes` non-empty
