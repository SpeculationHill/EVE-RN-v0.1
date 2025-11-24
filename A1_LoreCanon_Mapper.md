# A1_LoreCanon_Mapper

## Purpose
This program maps the core factions, empires, and canonical events of EVE's New Eden into a graph-friendly schema. The Universe of EVE is dominated by four major empires – the Amarr Empire, Caldari State, Gallente Federation and Minmatar Republic【414028640612414†L10-L16】. Each empire has a distinct political structure: the Amarr Empire is a theocratic monarchy and the largest nation in New Eden【94942924028785†L18-L23】; the Caldari State is run by megacorporations【944423758781733†L18-L24】; the Gallente Federation is liberal and vibrant【92673506518928†L18-L24】; and the Minmatar Republic is made up of determined tribal peoples who freed themselves after centuries of enslavement【833163296099247†L18-L28】. The mapper ingests canonical sources and represents factions, regions, organizations and major events as nodes with defined relationships.

## Data Schema
Define node types such as:
- **Empire**: id, name, description, government, population, home worlds.
- **Faction/Organization**: id, name, parentEmpire (nullable), type (e.g., pirate cartel, corporation), description.
- **Region/Constellation/System**: id, name, parentRegion, securityClass (highsec, lowsec, nullsec, wormhole)【482387685162354†L121-L125】.
- **Event**: id, name, date (YC* or real date), epoch (tag), summary, involved factions.
- **Source**: id, title, url, publication date.

Relationships:
- `BELONGS_TO`: Faction → Empire; System → Constellation → Region.
- `EVENT_INVOLVES`: Event → Faction/Empire.
- `LOCATED_IN`: System/Region/Constellation → Empire (sovereign).
- `DERIVED_FROM`: Node → Source.

## Implementation Notes
- Use a crawler to pull structured data from the EVE Universe site (e.g., the Empires pages) and community archives.
- Normalise names (e.g., “Amarr Empire” vs. “Dark Amarr”) and assign unique IDs.
- Parse narrative histories; for example, when the Amarr discovered interstellar travel and enslaved other races【94942924028785†L55-L68】, create an event with participants.
- Graph should be stored in a property graph database such as Neo4j or ArangoDB for easy traversal.
- Provide export functions (JSON-LD, GraphML) for integration with other layers.

## Example
When ingesting the Amarr Empire page, create an `Empire` node with attributes capturing its theocratic nature and size【94942924028785†L18-L23】. Create `Event` nodes like “Discovery of jump gate technology” and link them to the Amarr. Represent the Minmatar Rebellion as an event involving the Amarr and Minmatar tribes, with the date and outcome that billions of Minmatar were enslaved and later freed【833163296099247†L18-L28】.
