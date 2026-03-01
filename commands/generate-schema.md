---
description: Generate schema.org JSON-LD structured data markup for your real estate agent bio page. Produces ready-to-paste HTML markup including RealEstateAgent, AggregateRating, and FAQPage schemas.
allowed-tools: Read, Write, Edit, Glob
---

# Generate Schema Markup

Generate complete schema.org JSON-LD structured data for a real estate agent bio page. Uses the `schema-markup` skill.

## Process

1. **Collect data**: If the agent has already optimized their bio, pull data from there. Otherwise, collect:
   - Full name, job title, brokerage name and URL
   - Office address (street, city, state, ZIP)
   - Phone number and email
   - Headshot image URL (if available)
   - Website URL
   - Service area cities/counties
   - Professional designations (full names)
   - Specialties/expertise areas
   - Review rating and count (with platform)
   - Social media and platform profile URLs
   - Any awards
   - Languages spoken
   - Office hours

2. **Generate JSON-LD** using the RealEstateAgent schema template from the `schema-markup` skill.

3. **Generate supplementary markup**:
   - Open Graph meta tags
   - Meta description tag
   - BreadcrumbList schema (if the agent's site has navigation)
   - FAQPage schema (generate 3–5 common questions about the agent)

4. **Present the output** as:
   - Complete `<script type="application/ld+json">` block ready to paste
   - Open Graph `<meta>` tags ready to paste
   - Instructions on where to add the code
   - Links to validation tools

5. **Mark any missing data** with `[INSERT: description]` placeholders.

6. **Provide validation instructions**:
   - Test with Google Rich Results Test: https://search.google.com/test/rich-results
   - Validate with Schema.org Validator: https://validator.schema.org/

If `$ARGUMENTS` contains an agent name or bio text, use that to pre-populate the schema.
