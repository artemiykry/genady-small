# Incidents

An incident is a structured record of something going wrong — an outage, a security event, a botched release, a dropped ball. Separate from tasks because incidents have their own shape: a timeline, a resolution, and (later) a postmortem.

## Shape

Each incident has:
- **Title** — what happened, plainly
- **Status** — `open`, `postmortem`, `closed`
- **Started at / resolved at** — bookends
- **Owner** — the [person](people.md) driving the response
- **Owner team** — the [team](teams.md) on point
- **Timeline** — log of events, actions, observations with timestamps; entries can be edited or deleted as the picture sharpens
- **Action items** — [tasks](tasks.md) spawned from the incident

## Lifecycle

1. **Open** — captured the moment something breaks; lightweight to create. Timeline accrues as people work; action items become [tasks](tasks.md) linked to the incident.
2. **Postmortem** — once mitigated, status moves to `postmortem`. A [document](documents.md) is drafted; lessons surface.
3. **Closed** — postmortem published; follow-up tasks continue on their own. The incident itself is done.

## What you can do

- Append timeline entries quickly during response.
- See all incidents involving a team on their profile.

## What lives elsewhere

- The written-up lessons → [documents](documents.md) (the postmortem)
- The work that came out of it → [tasks](tasks.md), linked back
