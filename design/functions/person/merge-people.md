# merge_people

Combine two Person records into one.

## Input
- `keep` — the surviving person
- `drop` — the duplicate to absorb

## Output
- updated `keep` `Person`

## Side effects
- `drop.aliases` merged into `keep.aliases`
- `drop.contact` merged into `keep.contact` (`keep` wins on conflict)
- every backlink targeting `drop` rewritten to target `keep`
- `drop` deleted

## Preconditions
- both persons exist
- `keep ≠ drop`
