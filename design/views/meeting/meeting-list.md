# MeetingList

Meetings grouped by series or sorted by time.

- **Purpose** — find past notes; preview upcoming meetings.
- **Shows** — meeting rows with title, time, attendee count, series badge.
- **Actions** — `create_meeting`; open `MeetingPage`; group / sort.
- **States**
  - *upcoming* — future meetings only.
  - *past* — historical.
  - *by_series* — grouped by series.
- **Composed of** — meeting row, series header.
