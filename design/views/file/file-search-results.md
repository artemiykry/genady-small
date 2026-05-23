# FileSearchResults

Full-text search across the configured directory.

- **Purpose** — find files by content or path.
- **Shows** — matching files with ranked snippets.
- **Actions** — `search_files` (as user types); open match → `FilePreview` at match location.
- **States**
  - *idle* — empty query.
  - *searching* — query in flight.
  - *results* — matches shown.
  - *no_results* — empty state.
- **Composed of** — search input, result row, snippet.
