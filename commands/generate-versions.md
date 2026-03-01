---
description: Generate platform-specific bio versions tailored to each site's character limits, audience, and formatting rules. Supports Zillow, Google Business, Realtor.com, FastExpert, LinkedIn, personal websites, and social media.
allowed-tools: Read, Write, Edit, Glob
---

# Generate Platform Versions

Generate bio versions tailored to specific platforms. Uses the `platform-requirements` skill for specs.

## Process

1. **Check for existing optimized bio**: If the user has already run `/optimize-bio`, use those versions as the source material. If not, ask them to paste their optimized bio or run `/optimize-bio` first.

2. **Ask which platforms** they need versions for. Present the options:
   - Zillow (~3,000 chars)
   - Google Business Profile (750 chars — most critical for AI)
   - Realtor.com (~4,000 chars)
   - FastExpert (~2,000 chars)
   - LinkedIn About (2,600 chars) + Headline (220 chars)
   - Homes.com (~2,500 chars)
   - Facebook About (255 chars)
   - Instagram Bio (150 chars)
   - X/Twitter Bio (160 chars)

3. **Generate each requested version** respecting:
   - Character limits (include character count with each version)
   - Platform-specific audience and intent
   - Formatting rules (plain text vs. HTML)
   - Recommended opening hooks for each platform

4. **Present versions** clearly labeled with:
   - Platform name
   - Character count / character limit
   - Any platform-specific notes or tips

5. **Offer to update the profile tracker** with which versions were generated.

If `$ARGUMENTS` specifies platform names, generate for those platforms directly.
