# Take meeting notes

A scheduled meeting is starting; capture notes, decisions, and action items as they happen.

## Goal
Produce a Meeting record with notes, marked decisions, and action items captured during the session.

## Trigger
An Event on the calendar is approaching its start time; user opens it.

## Steps
1. **View:** `CalendarView` → click event → `EventDetail`.
2. **Function:** `attach_meeting_to_event(event)` — returns the Meeting (existing or newly created).
3. **View:** navigate to `MeetingPage` (state: *in_session*).
4. User types into the notes editor.
5. **Function:** `edit_meeting(meeting, notes)` — fires on save / autosave.
6. On a decision-worthy line: user invokes "Mark decision".
7. **Function:** `mark_meeting_decision(meeting, text)`.
8. On an action-item-worthy line: user invokes "Promote to action item" (inline ActionItem captured via `edit_meeting`).

## Postconditions
- `meeting.notes` reflects what was discussed.
- `meeting.decisions` contains the flagged lines.
- `meeting.action_items` lists any captured TODOs.

## Failure paths
- No event selected → user uses `create_meeting` instead (ad-hoc meeting).
