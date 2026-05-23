# EventDetail

Single event with source-owned metadata and local annotations.

- **Purpose** — present everything known about an event in one panel.
- **Shows** — title, time range, attendees (resolved where possible), source, annotations, attached meeting, linked entities.
- **Actions** — `annotate_event`, `link_event`, `attach_meeting_to_event`, `resolve_event_attendee`; open attached `MeetingPage`.
- **States**
  - *idle* — annotations rendered.
  - *annotating* — annotations editable.
- **Composed of** — `BacklinksPanel`.
