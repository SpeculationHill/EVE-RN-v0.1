# A4_EventCalendar_Schema

## Purpose
Describe the schema for indexing recurring community events such as fleets, classes, tournaments and seasonal celebrations.

## Event Fields
- `event_id`, `name`, `hostEntityId` (corp, alliance, community), `eventType` (e.g., Fleet, Class, Tournament, Social).
- `description`: Brief summary.
- `startTime` (UTC), `duration`, `recurrence` (e.g., weekly, monthly, one‑off).
- `location`: System or region (for in‑game events) or platform (Discord, Twitch).
- `audience`: Tags indicating intended participants (e.g., Newbro, Wormhole, PvP Learners).
- `requiredSkills` or recommended ships (if applicable).
- `registrationLink` (if required).
- `status`: Scheduled, Completed, Cancelled.

## Implementation Notes
- Use iCalendar or a similar standard to store recurrence rules.
- Pull event information from social channels and official calendars; for example, the public fleet pages provide instructions on form‑up times and channels【976944329353990†L146-L152】.
- Provide API endpoints for users to subscribe to calendars filtered by tags, time zone and activity.
