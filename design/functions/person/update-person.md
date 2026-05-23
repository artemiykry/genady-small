# update_person

Edit a person's attributes.

## Input
- `person`
- any subset of: `name`, `aliases`, `role`, `teams`, `contact`

## Output
- updated `Person`

## Side effects
- provided attributes updated

## Preconditions
- person exists
- if `name` provided, non-empty
- if `aliases` provided, unique within the person
