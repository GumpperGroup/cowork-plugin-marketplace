---
description: Analyze competing agents' bios and online presence to find positioning opportunities. Identifies gaps in competitor EEAT signals, unclaimed niches, and differentiation strategies you can use.
allowed-tools: Read, Write, Edit, Glob, WebFetch, WebSearch
---

# Analyze Competitors

Run a competitive bio analysis to identify positioning opportunities. Uses the `competitive-analysis` skill.

## Process

1. **Identify the agent and market**: Get the user's name, primary market, and specialties.

2. **Identify competitors**: Ask the user to name 3–5 direct competitors, or search for:
   - Top agents in their market on Zillow
   - Agents appearing in AI search results for their target queries
   - Agents in their brokerage or local association

3. **Analyze each competitor** using web search:
   - Find their bios across platforms
   - Assess bio content quality and EEAT signals
   - Count reviews and ratings
   - Identify their claimed specialties and positioning
   - Check for schema markup and technical optimization

4. **Generate the competitive analysis report** per the `competitive-analysis` skill format.

5. **Provide differentiation recommendations**:
   - Specific niches to claim
   - EEAT signals to emphasize
   - Query patterns to target
   - Positioning statements to consider

6. **Offer to incorporate findings** into bio optimization:
   - Rewrite bio with competitive positioning → `/optimize-bio`
   - Generate platform versions → `/generate-versions`

If `$ARGUMENTS` contains competitor names, begin the analysis directly.
