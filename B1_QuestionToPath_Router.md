# B1_QuestionToPath_Router

## Purpose
Design a program that interprets natural‑language questions from players and routes them to appropriate onboarding paths, activities and resources.

## Inputs & Outputs
- **Input**: Player query (e.g., “How do I make ISK as a beginner?” or “I want to try wormhole exploration”).  
- **Output**: Recommendations including archetype classification, suggested onboarding path stages, relevant tools and communities.

## Algorithm Overview
1. **Intent Detection**: Use NLP techniques (e.g., transformer models) to classify the query into intents such as “making ISK”, “PvP learning”, “industry”, or “exploration”.
2. **Archetype Inference**: Based on the query and any profile data, infer likely archetypes (e.g., the phrase “beginner” maps to Day‑1 Alpha).
3. **Activity Mapping**: Map intents to activities defined in A2_Activities_Taxonomy. For example, wormhole exploration queries map to Exploration activities【647673664077612†L154-L162】.
4. **Resource Selection**: Using the archetype and activity, select appropriate onboarding path stages (B1_Onboarding_Paths), tools (A3) and communities (A4). Include publicly accessible fleets for PvP learners【976944329353990†L113-L117】 or highlight relevant corp directories for industrialists.
5. **Explainable Output**: Return a structured response with recommended steps and the reasoning behind each recommendation.

## Considerations
- Support multi‑language queries; train or fine‑tune language models accordingly.
- Continuously learn from user feedback to improve routing accuracy (see C1_FeedbackLoop_Design).
- Maintain a knowledge base of frequently asked questions and pre‑built responses for efficiency.
