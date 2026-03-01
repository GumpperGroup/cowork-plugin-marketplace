---
name: profile-management
description: Track, manage, and maintain a list of URLs where a real estate agent's bio or profile appears online. Use when the user mentions profile URLs, tracking their online presence, wants to see where their bio lives, asks about their profiles, or says "where is my bio" or "my profiles". Also trigger when the user wants to add, remove, or update profile locations.
---

# Profile URL Management

Maintain a centralized tracker of every URL where an agent's bio or profile appears. This enables consistent updates, gap identification, and cross-platform auditing.

## Profile Tracker Format

Store and display the profile tracker as a structured table. When the user asks to see their profiles or manage their URLs, use this format:

```markdown
# Profile Tracker: [Agent Name]
Last Updated: [date]

| # | Platform | URL | Bio Version | Last Updated | Status | Notes |
|---|----------|-----|-------------|--------------|--------|-------|
| 1 | Personal Website | https://... | Website About | 2025-01-15 | ✅ Current | Primary bio page |
| 2 | Zillow | https://... | Zillow | 2025-01-10 | ✅ Current | 127 reviews |
| 3 | Google Business | https://... | GBP Short | 2024-11-20 | ⚠️ Stale | Needs 2025 stats |
| 4 | Realtor.com | https://... | Medium | 2024-08-01 | ❌ Outdated | Missing CRS designation |
| 5 | LinkedIn | https://... | LinkedIn | 2025-01-15 | ✅ Current | |
| 6 | FastExpert | https://... | — | — | 🔲 Not Set Up | Recommended |
| 7 | Facebook | https://... | Social Short | 2024-06-01 | ❌ Outdated | |
```

### Status Definitions
- ✅ **Current**: Bio updated within the last 6 months with accurate information
- ⚠️ **Stale**: Bio is 6–12 months old or has minor inaccuracies
- ❌ **Outdated**: Bio is over 12 months old or has significant inaccuracies
- 🔲 **Not Set Up**: Profile doesn't exist yet but is recommended

## Profile Management Workflows

### Adding a New Profile
When the user wants to add a URL:
1. Ask for the platform name and URL
2. Note which bio version is (or should be) used
3. Record the current date as "Last Updated"
4. Set status based on whether the bio is already optimized

### Updating Profile Status
When the user updates a bio on a platform:
1. Update the "Last Updated" date
2. Note which bio version was used
3. Change status to ✅ Current
4. Add any relevant notes

### Running a Profile Audit
Periodically review all tracked URLs:
1. Check each URL to verify it's still live
2. Compare the bio content against the latest optimized versions
3. Flag any inconsistencies across platforms
4. Update status column accordingly
5. Recommend any new platforms to add

## Recommended Platforms

For maximum AI search visibility, agents should have optimized profiles on:

### Tier 1 (Essential — Set Up First)
1. **Google Business Profile** — Most influential for AI Overviews
2. **Personal/Brokerage Website** — Primary authority page
3. **Zillow** — Highest consumer traffic
4. **Realtor.com** — NAR-connected, high domain authority

### Tier 2 (Important — Set Up Next)
5. **LinkedIn** — Professional authority, relocation referrals
6. **FastExpert** — Growing agent comparison site
7. **Homes.com** — Expanding consumer reach (CoStar-owned)

### Tier 3 (Supplementary — Good to Have)
8. **Facebook Business Page** — Local search and social proof
9. **Yelp** — Review authority
10. **Brokerage team page** — Internal authority signal
11. **Local Board/Association directory** — Institutional authority
12. **RateMyAgent** — Specialized review platform
13. **HomeLight** — Agent matching platform

### Tier 4 (Niche/Emerging)
14. **Nextdoor** — Hyper-local presence
15. **Instagram** (business profile) — Especially for luxury/lifestyle agents
16. **YouTube** (channel about) — For agents with video content
17. **Alignable** — B2B local business network

## Persistence

Since Cowork operates on local files, you can save and load the profile tracker as a markdown or JSON file in the user's working directory:

- Default filename: `profile-tracker.md` or `profile-tracker.json`
- Ask the user where they'd like to save it
- On subsequent sessions, offer to load the existing tracker
- If Google Drive MCP is connected, offer to save/sync there

## Gap Analysis

When reviewing the tracker, identify:
1. **Missing Tier 1 platforms** — Critical priority
2. **Outdated bios** — Update with latest optimized versions
3. **Inconsistent information** — Flag discrepancies across platforms
4. **Missing reviews** — Platforms with profiles but no reviews
5. **New platform opportunities** — Platforms the agent hasn't considered
