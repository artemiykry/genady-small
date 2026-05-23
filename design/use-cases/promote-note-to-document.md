# Promote a note to a document

A captured thought has matured into something I want to keep, structure, and link to.

## Goal
Convert a Note into a Document without losing references made to the note from elsewhere.

## Trigger
Author is reading a Note (in a `NotePage` view) and decides it deserves persistence.

## Steps
1. **View:** `NotePage` → user invokes "Promote to document" action.
2. **Function:** `promote_note_to_document(note)`.
   - **Effect:** new Document created with the note's body and a title derived from the first line.
   - **Effect:** backlinks targeting the Note are rewritten to target the new Document.
   - **Effect:** original Note is archived.
3. **View:** app navigates to `DocumentPage` for the new Document.

## Postconditions
- A new Document exists with the note's prior content.
- No entity still references the original Note (all backlinks now point at the Document).
- The original Note is archived (recoverable, but no longer in active surfaces).

## Failure paths
- Note is already archived → action disabled in `NotePage`.
- Note has already been promoted → idempotent; navigate to the existing Document.
