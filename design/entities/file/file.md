# File

A regular file on disk inside the configured directory. The app surfaces it; the filesystem owns it.

## Identity
- `path` — absolute path within the configured directory.

## Attributes
- **path** `string`
- **name** `string` — derived from `path`
- **type** `mime` — derived from extension or content
- **size** `bytes`
- **modified_at** `timestamp` — from the filesystem

## Invariants
- `path` is unique within the configured directory.
- The file exists on disk; the app does not store a copy.
- File contents are owned by the filesystem; external edits are reflected on next read.
