# edit_meeting

Update a meeting's mutable attributes.

## Input
- `meeting`
- any subset of: `title`, `agenda`, `notes`, `starts_at`, `ends_at`

## Output
- updated `Meeting`

## Side effects
- provided attributes updated
- backlinks recomputed from `agenda` and `notes`

## Preconditions
- meeting exists
- if both `starts_at` and `ends_at` provided, `starts_at` < `ends_at`
