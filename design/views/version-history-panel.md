# VersionHistoryPanel

Browse and restore prior versions of a versioned entity.

- **Purpose** — surface append-only edit history; allow preview and restore.
- **Shows** — chronological version list with `{timestamp, author}`.
- **Actions** — preview a version (read-only render); `restore_document_version`.
- **States**
  - *collapsed* — panel closed.
  - *list* — versions visible, none selected.
  - *previewing* — a version is rendered read-only.
