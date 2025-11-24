# DEV_Agent_Specs_EVE-RN

## Purpose
Describe high‑level specifications for AI agents that will power the EVE‑RN platform. These agents coordinate to harvest data, build the knowledge graph and deliver personalised guidance.

## Agents

1. **Indexer Agent**
   - **Role**: Harvest lore, system, tool and community data; normalise and tag according to taxonomies.
   - **Inputs**: RSS feeds of official sources, EVE University pages, forum posts, tool repositories.
   - **Outputs**: Structured updates for the knowledge graph; triggers for pipeline verification.
   - **Capabilities**: Scraping, data cleaning, natural language processing, ESI integration【119277652475160†L55-L59】.

2. **Journey Guide Agent**
   - **Role**: Answer player questions and guide them through onboarding paths (B1_QuestionToPath_Router).
   - **Inputs**: Player queries, archetype definitions, current graph state.
   - **Outputs**: Structured recommendations of activities, tools and communities; interactive dialogues.
   - **Capabilities**: Intent classification, dialogue management, retrieval‑augmented generation, feedback integration.

3. **Corp‑Match Agent**
   - **Role**: Match players to corporations/alliances or communities using PlaystyleToCorp_Matcher.
   - **Inputs**: Player preferences, corp directory.
   - **Outputs**: Ranked corp/community suggestions.
   - **Capabilities**: Multi‑criteria scoring, trust signal incorporation, fairness checks (no bias on sensitive data).

4. **Lore‑Canon Explainer Agent**
   - **Role**: Provide in‑depth lore explanations, summarise historical events and answer “why” questions.
   - **Inputs**: Lore graph, timeline index, sources.
   - **Outputs**: Explanations with citations to official lore.
   - **Capabilities**: Natural language generation, timeline synthesis.

## Architecture
- Agents communicate via shared data stores and event queues.
- Each agent’s actions are logged for accountability and debugging.
- Agents should respect user privacy and avoid unnecessary data retention.
