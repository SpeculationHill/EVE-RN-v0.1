# A4_CorpsAlliances_Directory

## Purpose
Define the data model and ingestion process for the directory of corporations and alliances. The directory should help players find groups that match their playstyle, time zone and goals.

## Schema
Each corp/alliance entry includes:
- `id`, `name`, `ticker`.
- `parentAllianceId` (for corps).
- `size` (number of members), `memberCorporations` (for alliances).
- `activityTags`: Tags from A2_Activities_Taxonomy (e.g., Mining, Faction Warfare, Wormholes).
- `playstyleTags`: e.g., Newbie‑Friendly, NPSI, RP, Industrial, PvP, PVE, Roleplay, Pirate.
- `timeZones`: List of active time zones (UTC offsets).
- `recruitmentStatus`: Open/Closed/Invite Only.
- `requirements`: SP requirements, voice comms, alt requirements.
- `communications`: Primary communications channels (Discord server invite, Mumble, TeamSpeak).
- `doctrines`: Preferred fleet compositions or philosophies.
- `description`, `links` (forum post, killboard, website).
- `trustRating` (computed from community feedback).

## Data Sources
- Official corp and alliance descriptions from the in‑game interface.
- Recruitment posts on the EVE forums and EVE University’s lists.
- Public fleet pages for NPSI groups【976944329353990†L113-L117】.
- Third‑party ranking services (e.g., zKillboard, EVEWho) for membership counts.

## Process
- Crawl the Recruitment Center of the EVE forums and parse corp posts for tags and time zones.
- Allow corp representatives to submit and update their information via a form.
- Verify submissions manually or via community trust signals before publishing.
