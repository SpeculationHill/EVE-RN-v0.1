# B1_PlaystyleToCorp_Matcher

## Purpose
Match players to corporations or alliances based on playstyle preferences, time zones, activity types and social factors.

## Inputs
- Player preferences: Preferred activities (e.g., mining, faction warfare), security class (highsec, lowsec, nullsec), risk tolerance, time zones, language, experience level, social preferences (hardcore vs. casual, roleplay vs. competitive).

## Matching Algorithm
1. **Tag Matching**: Compare player preferences against corp activityTags, playstyleTags and timeZones in the corp directory (A4_CorpsAlliances_Directory).
2. **Scoring Function**: Compute a similarity score using weighted criteria:
   - Activity overlap (e.g., mission running vs. mining).
   - Time zone overlap.
   - Corp size and newcomer friendliness.
   - Trust rating (A3_Tool_TrustSignals_Model analog for corps).
3. **Constraints**: Filter out corps that have closed recruitment or require minimum SP beyond the player’s level.
4. **Output**: Ranked list of corporations/alliances with rationale, plus direct links to recruitment posts or contact channels.

## Implementation Notes
- Provide adjustable weights so players can prioritise certain criteria.
- Include an option to match with NPSI communities for players not ready to commit to a corp【976944329353990†L113-L117】.
- Keep data up to date; integrate with corp submission forms and recruitment feed crawlers.
