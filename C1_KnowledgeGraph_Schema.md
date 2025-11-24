# C1_KnowledgeGraph_Schema

## Purpose
Define the top‑level schema that ties together all layers of the EVE-RN knowledge graph, linking lore, game systems, tools, communities and player journeys.

## High‑Level Entities
- **Empire/Faction/Organization**: As defined in A1_LoreCanon_Mapper.
- **Region/Constellation/System**: Spatial entities from A2_SolarSystem_GraphSchema.
- **Activity**: Nodes from A2_Activities_Taxonomy.
- **Ship/Class**: Entities from A2_ShipRole_Ontology.
- **Tool**: Entities from A3_ToolIndex_Harvester and categories from A3_Tool_Categories_Taxonomy.
- **Corp/Alliance/Community**: Entities from A4_CorpsAlliances_Directory and A4_Communities_Taxonomy.
- **Player Archetype**: Nodes from B1_Archetypes_Ontology.
- **Onboarding Stage**: Stage nodes from B1_Onboarding_Paths.
- **Event**: Lore or community events from A1_Epoch_Timeline_Index and A4_EventCalendar_Schema.
- **Transaction**: ISK flow entries from A2_ISKFlow_Model.

## Relationships
- `HAS_ACTIVITY`: Corp/Community ↔ Activity.
- `RECOMMENDS`: Archetype ↔ Tool, Community, Corp or Activity.
- `LOCATED_IN`: Corp/Alliance ↔ Region/System.
- `USES_TOOL`: Player ↔ Tool.
- `PARTICIPATES_IN`: Player ↔ Event.
- `BELONGS_TO`: Player ↔ Corp/Alliance or Community.
- `TAGGED_AS`: Entity ↔ Tag (from A1_Lore_TagTaxonomy).
- `CONNECTS`: System ↔ System (via stargates/wormholes)【647673664077612†L154-L162】.
- `FLOWED`: Transaction ↔ Activity (linking faucet/sink transactions to activities).

## Implementation Notes
- Use a property graph database; each node carries a `type` property referencing its layer.
- Ensure that unique IDs from each layer are globally unique, perhaps by prefixing with the layer (e.g., `A1:Empire:Amarr`).
- Provide an API to query across layers; e.g., find tools recommended for a PvP learner in wormhole space.
