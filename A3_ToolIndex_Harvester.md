# A3_ToolIndex_Harvester

## Purpose
Automatically harvest and normalise information about EVE third‑party tools, ensuring the index remains up‑to‑date. The EVE University wiki notes that there are a number of useful player‑made tools and lists the major, currently developed ones【26259959867812†L113-L116】. These include EVE OS, EVE-HR, Alliance Auth, SeAT, and many more.

## Harvesting Steps
1. **Seed Sources**: Start from curated lists such as the EVE University third‑party tools article【26259959867812†L113-L116】, GitHub repositories (e.g., awesome-eve), and official developer directories.
2. **Fetch Metadata**: For each tool, collect:
   - Name and version.
   - Description and primary function (e.g., fitting simulator, market aggregator, corp management).
   - Platform (web, desktop, mobile, Discord bot).
   - Data sources/APIs used (e.g., ESI, zKillboard, Dotlan).
   - Maintenance status: last update date, active development or archived.
   - Licence (proprietary, open source).
   - Community trust signals (see A3_Tool_TrustSignals_Model).
3. **Normalise**: Standardise names, categories and API references. Tools that provide multiple features (e.g., EVE OS) may appear in several categories.
4. **Store**: Save harvested data into a structured database with unique identifiers and link to categories defined in A3_Tool_Categories_Taxonomy.

## Considerations
- Use ESI’s API discovery endpoint【119277652475160†L55-L59】 to verify API scopes claimed by each tool.
- Implement update checks to revisit tool URLs periodically; handle unreachable or obsolete tools gracefully.
- Respect tool creators’ privacy and data usage guidelines; only collect publicly available information.
