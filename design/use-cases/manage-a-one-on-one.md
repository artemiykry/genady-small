# Manage a one-on-one over time

A recurring one-on-one with a colleague is a thread that runs across weeks — topics carry over, feedback compounds, follow-ups need tracking.

## Goal
The colleague's `brief` Document accumulates context across many meetings, with action items spawned as tasks, and recurring meetings linked into a series.

## Trigger
A recurring 1:1 Event syncs in from the calendar; the user opens it before the meeting.

## Steps

### Before
1. **View:** `CalendarView` → click upcoming 1:1 → `EventDetail`.
2. **Function:** `attach_meeting_to_event(event)` — returns Meeting linked to the existing series.
3. **View:** `PersonPage` for the colleague → review the `brief` Document.
4. User skims past meetings and pending follow-ups in `attended_meetings` and `assigned_tasks`.

### During
5. **View:** `MeetingPage` (state: *in_session*).
6. User types notes, captures decisions and action items (see use case 04).

### After
7. **Function:** `promote_action_item_to_task(meeting, i)` for each item (see use case 05).
8. **View:** `PersonPage` → open `brief` Document.
9. **Function:** `edit_document(brief, new_body)` — append any longer-term context: feedback themes, growth goals, ongoing topics.

## Postconditions
- The meeting is part of the series and linked to the person.
- Action items are real Tasks assigned to the colleague (or the user).
- `brief` Document reflects the evolving relationship, not just one meeting.

## Failure paths
- Person not yet in the graph → `resolve_event_attendee` first to bind the source attendee to a local Person.
