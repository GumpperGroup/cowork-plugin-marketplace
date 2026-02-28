---
description: Audit a bio page URL for AI search readiness. Checks structure, keywords, scannability, indexability, schema markup, and EEAT signals. Provide a URL to get a full audit report with a visibility score.
---

# Audit Bio Page

Perform a comprehensive audit of a bio page URL for AI search engine readiness.

## Process

1. **Get the URL**: If `$ARGUMENTS` contains a URL, use it. Otherwise ask the user for the URL to audit.

2. **Fetch and analyze the page** using web search to find the page content. Evaluate:

   **Content Analysis:**
   - Is the bio text present in crawlable HTML (not hidden in JavaScript or iframes)?
   - Is the content structured with proper headings?
   - Does it contain specific, factual EEAT signals?
   - Does it use natural language query patterns?
   - What is the approximate word count?

   **Technical Analysis:**
   - Is there schema.org/JSON-LD markup?
   - Are Open Graph meta tags present?
   - Is there a meta description?
   - Does the page title include the agent's name and location?
   - Are images alt-tagged with descriptive text?

   **Authority Analysis:**
   - Does the page link to review profiles?
   - Does it link to listings or market reports?
   - Is it linked from the brokerage's main site?
   - Does it have proper internal navigation?

3. **Score the page** using the visibility scoring rubric from the `ai-search-visibility` skill.

4. **Generate the audit report** in the format specified by the `ai-search-visibility` skill.

5. **Provide actionable recommendations** ordered by impact, with specific instructions for each fix.

6. **Offer next steps**:
   - Rewrite the bio with `/optimize-bio`
   - Generate schema markup with `/generate-schema`
   - Add this URL to the profile tracker with `/manage-profiles`
   - Run a competitive analysis with `/analyze-competitors`
