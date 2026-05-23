# set_person_status

Mark a person as active or former.

## Input
- `person`
- `status: enum(active, former)`

## Output
- updated `Person`

## Side effects
- `person.status ← status`

## Preconditions
- person exists
