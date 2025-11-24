# A3_Tool_TrustSignals_Model

## Purpose
Define a model for scoring the trustworthiness of third‑party tools to help users choose reliable, secure and actively maintained applications.

## Trust Signal Dimensions
1. **Maintenance**: Frequency of updates, responsiveness of developers to issues, whether the code is open source and contributions are accepted. Tools with recent commits and active issue trackers score higher.
2. **Community Adoption**: Number of users or installations, endorsements from respected groups (e.g., EVE University) and presence in curated lists【26259959867812†L113-L116】.
3. **Uptime & Reliability**: Historical availability, uptime percentage, and performance.
4. **Security & Privacy**: Use of official APIs (ESI)【119277652475160†L55-L59】, adherence to CCP’s third‑party developer policy, and minimal permissions requested.
5. **Reputation**: Reviews on forums and Discord, recommendations from content creators, and absence of reported scams or malicious behaviour.

## Scoring Method
- Assign each dimension a weight based on its importance; for example, Security & Privacy may carry 30%, Maintenance 25%, Adoption 20%, Uptime 15%, Reputation 10%.
- Normalise scores on a 0–100 scale.
- Tools below a minimum threshold should be flagged or excluded.
- Provide transparency: show users the breakdown of trust signals and allow them to override defaults.

## Implementation Notes
- Use GitHub APIs and website monitoring services to collect maintenance and uptime data.
- Analyse forum posts and Discord discussions using sentiment analysis to estimate reputation.
