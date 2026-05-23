# Merge duplicate person records

A person ended up in the graph twice — usually because a calendar attendee was auto-created with a slightly different identifier than an existing local Person.

## Goal
Collapse two Person records into one without losing any references.

## Trigger
User notices duplicates in `PeopleDirectory`.

## Steps
1. **View:** `PeopleDirectory` → select the canonical person → open `PersonPage`.
2. User invokes "Merge with…", picks the duplicate.
3. **Function:** `merge_people(keep, drop)`.
   - **Effect:** aliases and contact entries of `drop` absorbed into `keep`.
   - **Effect:** every backlink targeting `drop` rewritten to target `keep`.
   - **Effect:** `drop` deleted.
4. **View:** `PersonPage` for `keep` reloads with the merged data.

## Postconditions
- One Person exists where there were two.
- All prior references resolve to the kept Person.

## Failure paths
- Both records selected are the same person → action disabled.
