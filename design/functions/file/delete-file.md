# delete_file

Remove a file from disk.

## Input
- `file`

## Output
- none

## Side effects
- file removed from disk
- backlinks pointing at `file.path` become dangling

## Preconditions
- file exists on disk
