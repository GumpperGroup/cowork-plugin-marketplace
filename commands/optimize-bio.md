---
description: Optimize a real estate agent bio for AI search engines. Paste your current bio or provide your details, and get back a fully optimized version with EEAT signals, natural query phrasing, and entity-rich content.
allowed-tools: Read, Write, Edit, Glob, Grep
---

# Optimize Bio

You are running the bio optimization workflow. Follow these steps:

## Step 1: Collect Information

If the user has pasted a bio, analyze it. If not, ask for:

1. **Full name** (and any name variations used professionally)
2. **Brokerage** (full legal name)
3. **License state and year first licensed**
4. **Professional designations** (CRS, ABR, GRI, etc.)
5. **Primary service areas** (cities, counties, neighborhoods)
6. **Specialties** (buyer/seller, property types, niches)
7. **Stats**: Annual or career volume, transaction count, average price point
8. **Awards and recognition** (with awarding body and year)
9. **Review scores** (platform, rating, count — e.g., "4.9 on Zillow with 127 reviews")
10. **Languages spoken** (if other than English)
11. **Anything personal** they want included (background, community involvement, hobbies)

If they've pasted a bio, extract what you can and ask about anything missing.

## Step 2: Gap Analysis

Compare the provided information against the EEAT checklist from the `eeat-signals` skill. Present findings as:

```
### Bio Gap Analysis
✅ Strong: [list what's well-covered]
⚠️ Weak: [list what needs strengthening]
❌ Missing: [list what's absent and should be added]
```

## Step 3: Generate Optimized Bio

Produce the following versions using the `bio-optimization` and `platform-requirements` skills:

1. **Short** (25–40 words)
2. **Medium** (75–125 words)
3. **Long** (150–250 words)
4. **Website About** (250–400 words)

Present each version clearly labeled with word count.

## Step 4: Explain Changes

After presenting the versions, briefly explain:
- What key changes were made and why
- Which EEAT signals were strengthened
- What query patterns were incorporated
- Any data points that should be verified or updated

## Step 5: Offer Next Steps

Ask the user if they'd like to:
- Generate platform-specific versions (Zillow, Google Business, etc.)
- Generate schema.org markup for their website version
- Run a competitive analysis against other agents in their market
- Set up a profile tracker to manage where their bio appears
- Score their current AI search visibility

Use `$ARGUMENTS` as the initial bio text or agent details if provided.
