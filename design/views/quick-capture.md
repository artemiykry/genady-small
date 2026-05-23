# QuickCapture

Global modal for fast capture from anywhere.

- **Purpose** — get a thought out of the head into the app without context-switching.
- **Shows** — single body field; subtle type hint ("note by default; type `/` for commands").
- **Actions** — `create_note`; with slash-command, route to `create_task`, `create_meeting`, `create_incident`.
- **States**
  - *typing* — body buffer.
  - *command* — slash-command palette open over a `/` trigger.
- **Composed of** — body input, command palette popover.
