# remove_meeting_attendee

Remove a person from a meeting's attendee list.

## Input
- `meeting`
- `person`

## Output
- updated `Meeting`

## Side effects
- `person` removed from `meeting.attendees`

## Preconditions
- meeting exists
- person is currently an attendee
