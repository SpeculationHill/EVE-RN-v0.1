# C1_Metrics_Dashboard_Spec

## Purpose
Outline the metrics that should be tracked to measure the performance and impact of the EVE‑RN platform.

## Key Metrics
- **User Engagement**: Number of unique users, session length, returning visitors.
- **Query Statistics**: Volume of questions routed via B1_QuestionToPath_Router, distribution by archetype and activity, query success rate.
- **Tool & Resource Utilisation**: Click‑throughs to third‑party tools, corp recruitments, event RSVPs.
- **Corporation Matches**: Number of successful matches via PlaystyleToCorp_Matcher and subsequent corp joins.
- **Economic Analytics**: Changes in ISK faucet/sink volumes, as captured by the A2_ISKFlow_Model; correlation with recommended activities.
- **Feedback Scores**: User satisfaction ratings for recommendations; trust signal adjustments.

## Dashboard Design
- Use a web‑based dashboard with real‑time updates.
- Visualise trends with charts: line graphs for time series (ISK supply, queries), bar charts for top tools, pie charts for archetype distribution.
- Provide filters by time period, archetype, region, security class and event.
- Make metrics exportable (CSV/JSON) for further analysis.

## Data Sources
- Logging from user interactions with the EVE‑RN interface and API.
- Aggregated ISK flow metrics from the wallet journal (requires anonymous analytics).
- Survey responses and feedback loops (C1_FeedbackLoop_Design).
