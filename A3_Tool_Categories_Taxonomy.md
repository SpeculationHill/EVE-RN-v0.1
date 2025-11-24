# A3_Tool_Categories_Taxonomy

## Purpose
Establish a taxonomy for classifying third‑party tools by activity, role and data source. A clear taxonomy enables users to filter tools effectively and allows the recommender system to suggest appropriate tools for a given activity.

## Category Dimensions
- **Activity** (linked to A2_Activities_Taxonomy): Fitting, Market, Industry, Exploration, Fleet & PvP, Logistics, Corp Management, Community & Social, Intelligence (intel), Learning/Training.
- **Role**: 
  - *Simulator*: Tools that simulate ship fittings, e.g., PYFA.  
  - *Dashboard/Analytics*: Tools that visualise data or provide dashboards, e.g., MER dashboards.  
  - *Management*: Tools for corp/alliance management (e.g., EVE-HR, SeAT).  
  - *Market Intelligence*: Market data and trade calculators, e.g., Eve Market Data, Janice.  
  - *Alerting & Intel*: Killboard monitors, gatecamp alerts, wormhole mapping.
  - *Assistive Bot*: Discord bots or voice assistants.

- **Data Source**:
  - *ESI (EVE Swagger Interface)*【119277652475160†L55-L59】 – official REST API.  
  - *zKillboard* – kill statistics.  
  - *Dotlan* – maps and navigation.  
  - *SDE (Static Data Export)* – offline data sets.  
  - *Scraped Data* – where no official API is available (e.g., jita price watchers).

## Classification Rules
- A tool may belong to multiple activity categories and roles; e.g., EVE OS covers corp management, market data and navigation.
- Assign each tool a primary data source (the one most critical to its operation) and secondary sources.
- Use tags rather than a rigid hierarchy; categories should be extensible as new tool types emerge.
