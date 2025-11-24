# A1_Epoch_Timeline_Index

## Purpose
Provide a chronological index of major lore events for cross-linking with gameplay systems and community narratives. This index serves as the temporal backbone of the EVE-RN knowledge graph.

## Timeline Structure
Each entry should include: `event_id`, `event_name`, `epoch_tag`, `date` (approximate year in YC or years before YC), `summary`, and `sources`. Example epochs include:

- **Pre-Imperial Era**: Humanity colonises New Eden via the EVE Gate. Collapse of the EVE Gate isolates colonies (event `EVEGate_Collapse`).  
- **Amarr Expansion**: After recovering interstellar travel, the Amarr Empire began expanding and enslaving neighbouring nations【94942924028785†L55-L59】.  
- **Gallente–Caldari Divergence**: The Gallente Federation and Caldari State were once part of the same polity; ideological differences led to war and the Caldari founding their own state【944423758781733†L18-L24】【92673506518928†L54-L70】.  
- **Minmatar Enslavement and Rebellion**: Minmatar tribes were enslaved by the Amarr for over seven hundred years and later staged a rebellion that freed many of them【833163296099247†L18-L28】.  
- **Jove Contact and Drifters**: Encounters with the Jove and later Drifter threats; EDENCOM and the empires formed the New Eden Common Defense Initiative.  
- **Triglavian Invasion**: Triglavian Collective emerges from Abyssal Deadspace; EDENCOM established to fight back【775524039271374†L55-L66】.  

## Implementation Notes
- Use the tag taxonomy to assign `epoch_tag` to each event.
- Where possible, use official sources; for example, the Amarr Empire page notes their rediscovery of jump gate technology and subsequent expansion【94942924028785†L55-L59】.  
- The index should support multiple timelines (e.g., player-affected vs. canonical).
- Provide API endpoints to query events by epoch, faction, or keyword.
