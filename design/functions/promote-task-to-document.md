# promote_task_to_document

Convert a task into a document — when an intent has grown into something needing structure.

## Input
- `task`

## Output
- new `Document`

## Side effects
- new `Document` created via `create_document` with task's `title` and `body`
- backlinks targeting the task rewritten to target the document
- task is archived

## Preconditions
- task exists
- task not archived
