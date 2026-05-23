# NotePage

A single note in editor.

- **Purpose** — read or edit one note.
- **Shows** — title, body, created_at, updated_at.
- **Actions** — `edit_note`, `archive_note`, `restore_note`, `promote_note_to_task`, `promote_note_to_document`.
- **States**
  - *editing* — body editable.
  - *archived* — read-only.
- **Composed of** — `DocumentEditor`, `BacklinksPanel`.
