---
name: ai-search-visibility
description: Score and improve how likely a real estate agent's bio is to appear in AI-driven search results from ChatGPT, Google AI Overviews, Perplexity, Claude, and Grok. Use when the user asks about AI search visibility, wants to audit their online presence, asks "will AI recommend me?", mentions AI Overviews, or wants to understand how AI engines find and rank agents. Also use when auditing a bio page URL.
---

# AI Search Visibility Scoring & Auditing

AI search engines synthesize information differently than traditional search. This skill scores an agent's bio and web presence against the factors that determine whether AI will surface and recommend them.

## How AI Search Engines Find Agents

AI models build agent recommendations from multiple signals:

1. **Indexed Web Content**: Bios on crawlable pages (personal sites, Zillow, Realtor.com, Google Business)
2. **Structured Data**: Schema.org markup, JSON-LD, Open Graph tags
3. **Entity Consistency**: Same facts across multiple sources = higher confidence
4. **Review Aggregation**: Verified reviews on Google, Zillow, Yelp, Facebook
5. **Content Authority**: Blog posts, market reports, media mentions that establish expertise
6. **Freshness**: Recently updated content signals active practice
7. **Linkage**: Links from authoritative sources (MLS, association directories, news sites)

## Visibility Scoring Rubric

Score each category 0–10, then calculate a weighted total out of 100:

### 1. Bio Content Quality (Weight: 25%)
| Score | Criteria |
|-------|----------|
| 0–3 | Vague, no stats, no credentials, reads like marketing fluff |
| 4–6 | Some facts present but incomplete; missing key EEAT signals |
| 7–8 | Strong factual content; most EEAT signals present; good query matching |
| 9–10 | Exceptional: all EEAT signals, natural query phrasing, entity-rich, zero fluff |

### 2. Platform Coverage (Weight: 20%)
| Score | Criteria |
|-------|----------|
| 0–3 | Bio exists on 1–2 platforms only |
| 4–6 | Present on 3–5 platforms, some with weak or outdated bios |
| 7–8 | Present on 6+ platforms with consistent, optimized bios |
| 9–10 | Comprehensive coverage including niche platforms; all bios optimized and consistent |

### 3. Structured Data & Indexability (Weight: 15%)
| Score | Criteria |
|-------|----------|
| 0–3 | No schema markup; bio behind JavaScript; not indexable |
| 4–6 | Basic HTML bio page; no structured data; some crawlability issues |
| 7–8 | Clean HTML; schema.org LocalBusiness or Person markup; proper meta tags |
| 9–10 | Full JSON-LD RealEstateAgent schema; OpenGraph tags; sitemap inclusion; fast load |

### 4. Review Signals (Weight: 15%)
| Score | Criteria |
|-------|----------|
| 0–3 | Fewer than 10 reviews; no reviews on major platforms |
| 4–6 | 10–50 reviews; 4.0+ average; on 1–2 platforms |
| 7–8 | 50–100 reviews; 4.5+ average; on 3+ platforms |
| 9–10 | 100+ reviews; 4.7+ average; on 4+ platforms; recent reviews within 90 days |

### 5. Entity Consistency (Weight: 15%)
| Score | Criteria |
|-------|----------|
| 0–3 | Name/brokerage/stats differ across platforms; outdated info |
| 4–6 | Mostly consistent with some discrepancies |
| 7–8 | Highly consistent across all platforms; minor variations only |
| 9–10 | Perfect consistency; identical core facts everywhere; all platforms current |

### 6. Content Authority & Freshness (Weight: 10%)
| Score | Criteria |
|-------|----------|
| 0–3 | No content beyond bios; no blog, no market reports, no media |
| 4–6 | Some blog content or market reports; updated in last 12 months |
| 7–8 | Regular content; media mentions; updated in last 6 months |
| 9–10 | Active content publishing; recent media features; thought leadership; monthly updates |

## Bio Page Audit Process

When auditing a specific URL:

1. **Fetch the page** using web search or provided URL
2. **Check indexability**: Is the page likely crawlable? Is the bio rendered in HTML (not locked in JavaScript/iframe)?
3. **Evaluate structure**: Are there proper headings? Is the bio in a logical reading order?
4. **Check for structured data**: Look for schema.org markup, JSON-LD, Open Graph meta tags
5. **Assess content quality**: Score against the Bio Content Quality rubric above
6. **Check page speed signals**: Heavy images, third-party scripts, render-blocking resources
7. **Review internal linking**: Does the page link to reviews, listings, blog content?
8. **Cross-reference**: Search for the agent's name to see what other sources AI would find

## Audit Report Format

Present findings as:

```
## AI Search Visibility Audit: [Agent Name]
**URL**: [audited URL]
**Date**: [today's date]
**Overall Score**: [X]/100

### Scores by Category
| Category | Score | Weight | Weighted |
|----------|-------|--------|----------|
| Bio Content Quality | X/10 | 25% | X |
| Platform Coverage | X/10 | 20% | X |
| Structured Data | X/10 | 15% | X |
| Review Signals | X/10 | 15% | X |
| Entity Consistency | X/10 | 15% | X |
| Content Authority | X/10 | 10% | X |
| **Total** | | | **X/100** |

### Key Findings
[Bulleted list of top 3 strengths and top 3 improvement areas]

### Priority Recommendations
[Numbered list, highest impact first]
```

## Improvement Recommendations by Score Range

- **0–30 (Critical)**: Bio needs a complete rewrite. Start with the `bio-optimization` skill.
- **31–50 (Needs Work)**: Core content exists but has major gaps. Focus on EEAT signals and platform expansion.
- **51–70 (Moderate)**: Good foundation. Focus on structured data, consistency, and review growth.
- **71–85 (Strong)**: Well-optimized. Focus on content authority, freshness, and niche platform coverage.
- **86–100 (Excellent)**: Maintain momentum. Focus on ongoing content, recent reviews, and emerging platforms.
