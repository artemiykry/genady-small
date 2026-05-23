# Convert meeting action items to tasks

After a meeting, turn the action items into tracked tasks so they don't get lost.

## Goal
Each ActionItem flagged in a Meeting becomes a Task that surfaces in the user's task views.

## Trigger
User is on `MeetingPage` (state: *after*) reviewing the action items list.

## Steps
1. **View:** `MeetingPage` shows action items.
2. For each item, user clicks "Promote to task".
3. **Function:** `promote_action_item_to_task(meeting, action_item_index)`.
   - **Effect:** new Task created with title, assignee, due_date from the action item.
   - **Effect:** `meeting.action_items[i].promoted ← task`.
   - **Effect:** task gains a backlink to the meeting.
4. **View:** action item row updates to show "↗ Task" link.

## Postconditions
- Every promoted action item references a real Task.
- Re-promoting is idempotent — returns the same task.

## Failure paths
- Action item already promoted → returns existing task; no duplicate.
