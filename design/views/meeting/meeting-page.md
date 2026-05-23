# MeetingPage

A meeting with agenda, notes, decisions, and action items.

- **Purpose** — single working surface during and after a meeting.
- **Shows** — title, time, attendees, agenda, notes, decisions, action items, linked event.
- **Actions** — `edit_meeting`, `add_meeting_attendee`, `remove_meeting_attendee`, `mark_meeting_decision`, `promote_action_item_to_task`, `attach_meeting_to_event`, `detach_meeting_from_event`, `summarize_meeting`.
- **States**
  - *preparing* — before start time; agenda focused.
  - *in_session* — within scheduled time; notes focused.
  - *after* — past meeting; recap and action items focused.
- **Composed of** — `DocumentEditor` (notes/agenda), action-item row, decision list, `BacklinksPanel`.
