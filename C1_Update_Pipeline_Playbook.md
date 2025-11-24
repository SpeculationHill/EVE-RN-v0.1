# C1_Update_Pipeline_Playbook

## Purpose
Describe the process by which new tools, corporations, lore updates and community resources are discovered, verified and integrated into the EVE‑RN knowledge graph.

## Pipeline Stages
1. **Discovery**
   - Monitor official sources (EVE Universe pages, dev blogs, Monthly Economic Reports) for new lore or game mechanics.
   - Watch curated lists like the EVE University third‑party tools article【26259959867812†L113-L116】 for new tool releases.
   - Crawl the Recruitment Center and public fleet announcements for new communities.
   - Accept user submissions via forms or GitHub pull requests.

2. **Verification**
   - Cross‑reference submissions with official sources; confirm facts using citations (e.g., verifying empire attributes from EVE Universe pages【414028640612414†L10-L16】).
   - Check tool repositories for recent activity and proper API usage【119277652475160†L55-L59】.
   - Validate corp/alliance information by contacting recruiters or checking in‑game corp descriptions.

3. **Classification**
   - Tag entities using the appropriate taxonomies (A1 tags, A2 activities, A3 tool categories, A4 community types).
   - Determine security class for systems based on true security numbers【482387685162354†L121-L125】.
   - Assign events to epochs and arcs.

4. **Integration**
   - Ingest verified data into the graph with unique IDs.
   - Link new entities with existing ones (e.g., a new wormhole community linked to wormhole systems and exploration activities).
   - Update caches and derived artefacts (e.g., the API capability matrix).

5. **Publication**
   - Generate changelogs; summarise new additions for transparency.
   - Notify relevant agents (Indexing Agent, Journey Guide Agent) to incorporate new knowledge.

## Governance
- Maintain a moderation team to review controversial or sensitive additions.
- Schedule regular review cycles to archive obsolete entities or update trust ratings.
