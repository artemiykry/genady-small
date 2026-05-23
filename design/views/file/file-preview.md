# FilePreview

Inline viewer for common file types.

- **Purpose** — read or skim a file without leaving the app.
- **Shows** — rendered content per type (text/markdown/code highlighting, PDF page-by-page, image, audio/video player).
- **Actions** — `open_file_externally`; for editable types, hand off to an editor that calls `edit_file`.
- **States**
  - *loading* — fetching content.
  - *rendered* — content shown.
  - *unsupported* — fallback with "open externally" suggestion.
  - *error* — read failed.
- **Composed of** — type-specific renderer.
