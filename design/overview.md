# Overview

A single-user desktop app that unifies the artifacts of knowledge work — tasks, calendar, meetings, notes, documents, people — into one connected workspace, with an agent that can read and act on all of it.

## Core ideas

- **One graph, many shapes.** Everything (task, note, doc, meeting, incident, person, team, event) is a first-class entity in the same graph. You move between them by linking and mentioning — not by switching apps.
- **Capture first, organize later.** Friction at capture is the enemy. Anything can start as a scribble and grow into a task, doc, or meeting note.
- **Links are the connective tissue.** Mention a person, link a doc, embed a task. Everything is reachable by following references — there is no hashtag layer in between.
- **The agent is a peer, not a feature.** It can see what you see, write what you can write, and works alongside you in chat or proactively.
- **Local-first, calmly synced.** Your stuff lives on your machine. External calendars sync in; nothing else leaves unless you ask.

## The pieces

- [Tasks](entities/tasks.md) — work, infinitely nestable, viewable as outline-table or gantt
- [Calendar](entities/calendar.md) — time, synced with the outside
- [Meetings](entities/meetings.md) — notes anchored to calendar events
- [Incidents](entities/incidents.md) — structured records of things going wrong
- [Notes](entities/notes.md) — quick, lightweight capture
- [Documents](entities/documents.md) — long-form, durable knowledge
- [Files](entities/files.md) — tree, viewer, and search over a directory on disk
- [People](entities/people.md) — colleagues, with overview, one-on-ones, and plans
- [Teams](entities/teams.md) — hierarchical groups of people
- [Agent](agent/overview.md) — chat that can act

## What this app is not

- Not a team collaboration tool. Single user.
- Not a wiki, not a project manager, not an email client — though it touches the same problems.
- Not cloud-first. The app works offline.
