# promote_action_item_to_task

Convert a meeting action item into a tracked task.

## Input
- `meeting`
- `action_item_index: int`

## Output
- `Task` (new, or existing if already promoted)

## Side effects
- new `Task` created via `create_task` with `title`, `assignee`, `due_date` from the action item
- `meeting.action_items[action_item_index].promoted ← task`
- task gains a backlink to the meeting

## Preconditions
- meeting exists
- `action_item_index` valid
- idempotent — if already promoted, returns the existing task
