# CalendarView

Timeline of upcoming and recent events from synced calendars.

- **Purpose** — see what's coming up; click into an event for context.
- **Shows** — events laid out by start time; today highlighted; multi-day events span cells.
- **Actions** — open `EventDetail`; `annotate_event` via inline shortcut; `attach_meeting_to_event` from context menu.
- **States**
  - *month* — calendar grid.
  - *week* — agenda-style week view.
  - *day* — hour-by-hour single day.
  - *empty* — no events in range.
- **Composed of** — event chip.
