# DocumentPage

The single screen for reading, editing, and navigating one document.

- **Purpose** — present a document with its content, history, and graph neighbors in one place.
- **Shows** — title, body (rendered or editable), `updated_at`, version count, backlinks.
- **Actions** — `edit_document`, `restore_document_version` (from history panel), open any linked entity.
- **States**
  - *reading* — body rendered; editor closed.
  - *editing* — body editable; unsaved buffer; save commits via `edit_document`.
  - *history* — version list visible; selecting a version previews it; "restore" calls `restore_document_version`.
- **Composed of** — `DocumentEditor`, `VersionHistoryPanel`, `BacklinksPanel`.
