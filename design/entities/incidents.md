# Incidents

An incident is a structured record of something going wrong — an outage, a security event, a botched release, a dropped ball. Separate from tasks because incidents have their own shape: a timeline, a severity, a resolution, and (later) a postmortem.

## Shape

Each incident has:
- **Title** — what happened, plainly
- **Severity** — `sev1` / `sev2` / `sev3` / `sev4`
- **Status** — `ongoing`, `mitigated`, `resolved`, `postmortem`
- **Started at / resolved at** — bookends
- **Owner** — the [person](people.md) driving the response
- **Responders** — other people involved
- **Timeline** — append-only log of events, actions, observations (with timestamps)
- **Links** — tasks spawned, docs, meetings, files

## Lifecycle

1. **Open** — captured the moment something breaks; lightweight to create.
2. **Respond** — timeline accrues as people work. Action items become [tasks](tasks.md) linked to the incident.
3. **Resolve** — mitigation succeeds; the incident closes.
4. **Postmortem** — a [document](documents.md) is drafted; lessons surface; follow-up tasks track to completion.

## What you can do

- Open an incident from anywhere — global hotkey, agent (*"we have an incident"*).
- Append timeline entries quickly during response.
- Convert a timeline item into a [task](tasks.md) with one keystroke.
- View incidents on the [calendar](calendar.md) by start time.
- See all incidents involving a person on their profile.

## What lives elsewhere

- The written-up lessons → [documents](documents.md) (the postmortem)
- The work that came out of it → [tasks](tasks.md), linked back
