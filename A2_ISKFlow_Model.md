# A2_ISKFlow_Model

## Purpose
Model the flow of ISK (the in‑game currency) through faucets (sources) and sinks (destruction mechanisms) and link them to activities and tools. Understanding ISK flows is essential for economic analysis and recommending profitable activities.

## Concepts
- **ISK Faucet**: A mechanic that creates ISK out of nothing and deposits it into players’ wallets. Examples include insurance payouts and NPC bounties【940571151247159†L31-L38】. The biggest faucet is the bounty system, rewarding players for destroying NPC pirate ships in missions and exploration sites【940571151247159†L67-L74】. Agent mission rewards and sales to NPC buy orders are also faucets【940571151247159†L67-L76】.
- **ISK Sink**: A mechanic that removes ISK from the game permanently. Common sinks include sales taxes and broker fees, cloning fees, insurance purchase fees, and purchasing items from NPC corporations【940571151247159†L83-L101】.  
- **Transfer**: Player‑to‑player transactions, such as market trades and contracts; these do not create or destroy ISK but redistribute it.

## Data Model
- **Transaction**: `id`, `timestamp`, `type` (Faucet/Sink/Transfer), `category` (e.g., bounty, tax, insurance), `amount`, `sourceCharacterId`, `destinationCharacterId`, `relatedActivity`.  
- **Aggregations**: Daily/weekly totals per faucet and sink type, region and activity.  
- **Linking to Activities**: For each activity (from A2_Activities_Taxonomy), specify typical ISK faucets and sinks. For example, mission running yields bounty and mission reward faucets; market trading involves tax sinks.

## Implementation Plan
- Use the ESI market and wallet endpoints【119277652475160†L55-L59】 to collect anonymised wallet journal data (requires proper scopes and user consent).
- Combine with aggregated data from CCP’s Monthly Economic Reports to calibrate the model; these reports discuss faucet and sink balance and inflation.
- Provide visualisations: bar charts of top faucets and sinks, line charts of total ISK supply over time.
- Expose API endpoints for querying the ISK flow data (e.g., faucets by activity, sinks per region).
