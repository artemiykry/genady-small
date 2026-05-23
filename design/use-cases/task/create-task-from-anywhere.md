# Create a task from anywhere

Sometimes a thought is intent, not a note — capture it directly as a task.

## Goal
Create a Task without leaving the current context.

## Trigger
User hits the global hotkey, then types `/task ` followed by a title.

## Steps
1. **View:** `QuickCapture` opens.
2. User types `/`; the command palette opens (state: *command*).
3. User selects `task`, types the title, hits enter.
4. **Function:** `create_task(title)`.
5. **View:** `QuickCapture` closes; toast confirms with a link to `TaskPage`.

## Postconditions
- A new Task exists with `status = todo`, `priority = none`.

## Failure paths
- User cancels → no Task created.
- Empty title after `/task ` → action disabled until non-empty.
