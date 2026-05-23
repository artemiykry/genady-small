# create_person

Add a person to the local entity graph.

## Input
- `name: string`
- `aliases: string[]?`
- `role: string?`
- `contact: map<string, string>?`

## Output
- new `Person`

## Side effects
- new `Person` persisted with `status = active`
- empty `brief` Document auto-created and linked

## Preconditions
- `name` non-empty
- aliases unique within the person
