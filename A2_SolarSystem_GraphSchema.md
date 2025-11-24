# A2_SolarSystem_GraphSchema

## Purpose
Define the schema used to represent solar systems, stargates and spatial relationships within the EVE-RN knowledge graph. Systems are grouped into constellations and regions and have security classifications that determine gameplay mechanics.

## Entities and Attributes
- **Region**: `region_id`, `name`, `securityClass` (EmpireSpace, LowSecurity, NullSecurity, WormholeSpace), `description`.
- **Constellation**: `constellation_id`, `name`, `region_id`.
- **SolarSystem**: `system_id`, `name`, `constellation_id`, `true_sec` (numeric from –1.0 to 1.0), `securityClass`. According to the EVE University article on system security, high‑sec systems have security level between 0.5 and 1, low‑sec between 0.1 and 0.4, null‑sec between –1 and 0, and wormhole space has a security level of –1【482387685162354†L121-L125】.  
- **Stargate**: `gate_id`, `from_system_id`, `to_system_id`, `type` (permanent/wormhole), `maxJumpRange`.
- **Station/Structure** (optional): `structure_id`, `type`, `ownerCorpId`, `system_id`.

## Relationships
- `CONTAINS`: Region→Constellation→SolarSystem.
- `CONNECTED_TO`: SolarSystem↔SolarSystem via Stargate.
- `SOVEREIGNTY`: SolarSystem→Empire/Alliance.
- `HAS_STRUCTURE`: SolarSystem→Station/Structure.

## Implementation Notes
- Derive `securityClass` from `true_sec` using thresholds defined above【482387685162354†L121-L125】.
- Model wormholes as special `Stargate` entities with temporary lifetimes and a property `expires_at`.
- Include fields for jump gates, triglavian conduits and other navigation features.
