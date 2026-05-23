# search_files

Full-text search across file contents.

## Input
- `query: string`
- `filter: { type?: mime, path_prefix?: string }?`

## Output
- `File[]` with match locations

## Side effects
- none (read-only against the index)

## Preconditions
- search index is built or buildable on demand
