# edit_file

Write new content to an existing file.

## Input
- `file`
- `content: bytes`

## Output
- updated `File`

## Side effects
- writes `content` to `file.path` on disk
- `modified_at` updated to the new filesystem mtime

## Preconditions
- file exists on disk
