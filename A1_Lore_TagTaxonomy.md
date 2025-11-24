# A1_Lore_TagTaxonomy

## Purpose
Define a controlled vocabulary (tag taxonomy) for categorising lore entities: factions, epochs, regions, NPC corporations, and story arcs. Tags enable consistent classification across datasets and facilitate search and recommendation.

## Tag Dimensions
- **Empire Tags**: `Amarr`, `Caldari`, `Gallente`, `Minmatar` (the four major empires)【414028640612414†L10-L16】.
- **Organization Types**: `PirateCartel`, `Corporation`, `ReligiousCult`, `Alliance`, `IndependentNation`.
- **Epoch Tags**: Chronological periods in New Eden history, e.g., `FirstEmpire` (Amarr expansion era【94942924028785†L55-L68】), `Gallente–Caldari War`, `Minmatar Rebellion`【833163296099247†L18-L28】, `TriglaviansEncounter`.
- **Region Tags**: high-level divisions such as `EmpireSpace`, `LowSecurity`, `NullSecurity`, `WormholeSpace` (the system security classes of 0.5–1, 0.1–0.4 and –1–0 respectively【482387685162354†L121-L125】).
- **Story Arc Tags**: e.g., `SanshaNation`, `Drifters`, `TriglavianInvasion`, representing major narrative arcs or expansions.
- **NPC Corporation Tags**: Use patterns like `Corp:Kaalakiota` or `Corp:ORE` to keep corp names distinct; link to parent empires where appropriate (e.g., Kaalakiota belongs to the Caldari State【944423758781733†L18-L24】).

## Guidelines
- Tags are case-insensitive but should be stored in canonical form.
- Each entity can have multiple tags (e.g., Sansha’s Nation: `PirateCartel`, `StoryArc:Sansha`).
- Use epoch tags to slice the timeline for time-based queries.
- Maintain a registry of tags with definitions and synonyms.
