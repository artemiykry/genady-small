# Capture a quick thought

A thought arrives mid-task; get it into the app without losing context.

## Goal
Persist a piece of text as a Note in under one second of friction.

## Trigger
User hits the global hotkey from anywhere on the OS.

## Steps
1. **View:** `QuickCapture` opens centered, focus on body.
2. User types the thought; hits enter.
3. **Function:** `create_note(body)`.
4. **View:** `QuickCapture` closes; toast confirms with a link to `NotePage`.

## Postconditions
- A new active Note exists with the typed body.
- The user's prior application context is untouched.

## Failure paths
- User cancels (Esc) → no Note created.
