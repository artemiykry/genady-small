# mark_meeting_decision

Flag a piece of text in meeting notes as a decision.

## Input
- `meeting`
- `text: string`

## Output
- updated `Meeting`

## Side effects
- `text` appended to `meeting.decisions`

## Preconditions
- meeting exists
- `text` non-empty
