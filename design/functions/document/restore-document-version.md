# restore_document_version

Promote a historical version to current.

## Input
- `document`
- `version_index: int`

## Output
- updated `Document`

## Side effects
- calls `edit_document(document, versions[version_index].body)`
- the restore is itself a new edit, not a rewind

## Preconditions
- `version_index` is a valid offset into `document.versions`
