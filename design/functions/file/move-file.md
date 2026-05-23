# move_file

Move or rename a file on disk.

## Input
- `file`
- `new_path: string`

## Output
- updated `File`

## Side effects
- file moved on disk from `file.path` to `new_path`
- backlinks pointing at the old `path` are rewritten to `new_path`

## Preconditions
- file exists
- `new_path` is within the configured directory
- no file exists at `new_path`
