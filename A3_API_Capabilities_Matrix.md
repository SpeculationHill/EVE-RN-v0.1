# A3_API_Capabilities_Matrix

## Purpose
Provide a matrix describing which APIs or data sources each tool uses and what capabilities they provide. This helps developers understand integration points and allows the system to check for necessary scopes.

## Matrix Structure
For each tool harvested by A3_ToolIndex_Harvester, record:
- `tool_id`, `name`.
- `supports_ESI` (Yes/No) – uses the official ESI API【119277652475160†L55-L59】.
- `uses_SSO` (Yes/No) – requires player authentication (SSO).  
- `zKill` – uses zKillboard killmail feeds.
- `Dotlan` – consumes Dotlan map APIs.
- `Other` – other data sources (e.g., EVE Gatecamp Check, Siggy, Tripwire).
- `Read/Write` – whether the tool performs read-only or modifies data via ESI; many endpoints require authentication【119277652475160†L63-L66】.
- `Scopes` – list of required ESI scopes (wallet, assets, fitting, etc.)

## Implementation Notes
- Use ESI’s API Explorer or metadata endpoints to verify available scopes and whether they are read or write【119277652475160†L55-L70】.
- Tools requiring write scopes should be highlighted as higher risk and flagged for user consent in the recommender.
- The matrix should be automatically generated and updated as part of the harvester pipeline.
