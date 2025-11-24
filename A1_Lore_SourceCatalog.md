# A1_Lore_SourceCatalog

## Purpose
Maintain a catalogue of official lore sources with stable identifiers to ensure that data ingestion and citations remain consistent.

## Source Types
- **Official Universe Pages**: Faction and empire pages on the EVE Universe site (e.g., the Empires page which states that New Eden is dominated by four major empires【414028640612414†L10-L16】).  
- **Empire Detail Pages**: Detailed pages for the Amarr Empire, Caldari State, Gallente Federation and Minmatar Republic, describing their government structures and history【94942924028785†L18-L23】【944423758781733†L18-L24】【92673506518928†L18-L24】【833163296099247†L18-L28】.  
- **Chronicles**: Short stories and lore essays published by CCP.  
- **Dev Blogs / News**: Posts on eveonline.com that describe events like the Triglavian invasion, EDENCOM formation and economic reports.  
- **EVE University and player wikis**: Secondary but well‑maintained resources covering systems such as security classes【482387685162354†L115-L125】 and third-party tools【26259959867812†L113-L116】.  
- **Official PDFs / E-books**: Mark726's Lore Survival Guide and the interactive timeline.

## Fields
For each source, store: `source_id`, `title`, `url`, `publication_date`, `type`, `description`. Use consistent naming and include captured citation IDs for reproducibility.

## Maintenance
- Periodically validate that URLs are still reachable; if a URL changes, update the catalog but keep the old ID for reference.
- Tag each source with relevant epochs, factions and topics to improve discovery.
