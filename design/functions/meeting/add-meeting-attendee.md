# add_meeting_attendee

Add a person to a meeting's attendee list.

## Input
- `meeting`
- `person`

## Output
- updated `Meeting`

## Side effects
- `person` appended to `meeting.attendees`

## Preconditions
- meeting exists
- person exists
- person not already an attendee
