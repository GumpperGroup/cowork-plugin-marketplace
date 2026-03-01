---
description: Score your overall AI search visibility across all platforms using a weighted rubric covering bio quality, platform coverage, structured data, reviews, entity consistency, and content authority. Get a score out of 100 with specific improvement priorities.
allowed-tools: Read, Write, Edit, Glob, WebFetch, WebSearch
---

# Score AI Visibility

Run a comprehensive AI search visibility assessment. Uses the `ai-search-visibility` skill.

## Process

1. **Gather inputs**: Collect the agent's name, primary market, and either:
   - Their profile tracker (if `/manage-profiles` has been used)
   - A list of URLs where their bio appears
   - Just their name and market (Claude will search for their profiles)

2. **Evaluate each scoring category** per the `ai-search-visibility` rubric:
   - Bio Content Quality (25%)
   - Platform Coverage (20%)
   - Structured Data & Indexability (15%)
   - Review Signals (15%)
   - Entity Consistency (15%)
   - Content Authority & Freshness (10%)

3. **Calculate weighted total** out of 100.

4. **Generate the full audit report** including:
   - Score table with individual and weighted scores
   - Top 3 strengths
   - Top 3 improvement areas
   - Priority recommendations ordered by impact

5. **Provide score interpretation**:
   - 0–30: Critical — complete overhaul needed
   - 31–50: Needs Work — major gaps to address
   - 51–70: Moderate — good foundation, focus on gaps
   - 71–85: Strong — optimize and maintain
   - 86–100: Excellent — maintain momentum

6. **Recommend specific next steps** based on the lowest-scoring categories, connecting to other plugin commands:
   - Low bio quality → `/optimize-bio`
   - Low platform coverage → `/manage-profiles`
   - No structured data → `/generate-schema`
   - Low reviews → Provide review generation strategy
   - Inconsistent entities → Generate consistency checklist

If `$ARGUMENTS` contains an agent name or URL, start the assessment directly.
