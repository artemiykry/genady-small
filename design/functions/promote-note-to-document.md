# promote_note_to_document

Convert a Note into a Document, preserving incoming references.

## Input
- `note`

## Output
- new `Document`

## Side effects
- new `Document` created with note's `body` and a title derived from the first line
- every backlink targeting the note is rewritten to target the new Document
- original note is archived

## Preconditions
- note exists
- note is not archived
