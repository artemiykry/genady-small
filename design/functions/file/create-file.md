# create_file

Write a new file to disk inside the configured directory.

## Input
- `path: string`
- `content: bytes`

## Output
- new `File`

## Side effects
- writes `content` to `path` on disk
- new `File` becomes visible on next index pass

## Preconditions
- `path` is within the configured directory
- no file exists at `path`
