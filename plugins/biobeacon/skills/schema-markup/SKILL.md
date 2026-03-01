---
name: schema-markup
description: Generate schema.org JSON-LD structured data markup for real estate agent bio pages. Use when the user mentions schema, structured data, JSON-LD, rich snippets, markup, or asks how to make their bio page machine-readable for search engines and AI. Also use when generating the Website About version of a bio, as schema markup should accompany it.
---

# Schema.org Structured Data for Real Estate Agent Pages

Structured data markup helps AI search engines and traditional search engines understand your bio page as a structured entity rather than just text on a page. This is one of the highest-impact technical optimizations for AI visibility.

## Primary Schema: RealEstateAgent

The `RealEstateAgent` type is a sub-type of `LocalBusiness` in schema.org. It tells search engines "this page is about a real estate professional" with machine-readable facts.

### Complete JSON-LD Template

Generate this markup customized with the agent's actual data:

```json
{
  "@context": "https://schema.org",
  "@type": "RealEstateAgent",
  "name": "[Agent Full Name]",
  "description": "[Short bio version — 1-2 sentences]",
  "url": "[Agent's primary website URL]",
  "image": "[Agent headshot URL]",
  "telephone": "[Phone number in +1-XXX-XXX-XXXX format]",
  "email": "[Email address]",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "[Office street address]",
    "addressLocality": "[City]",
    "addressRegion": "[State abbreviation]",
    "postalCode": "[ZIP]",
    "addressCountry": "US"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": "[Latitude]",
    "longitude": "[Longitude]"
  },
  "areaServed": [
    {
      "@type": "City",
      "name": "[City Name]",
      "containedInPlace": {
        "@type": "State",
        "name": "[State]"
      }
    }
  ],
  "employee": {
    "@type": "Person",
    "name": "[Agent Full Name]",
    "jobTitle": "REALTOR®",
    "worksFor": {
      "@type": "RealEstateAgent",
      "name": "[Brokerage Name]",
      "url": "[Brokerage URL]"
    },
    "hasCredential": [
      {
        "@type": "EducationalOccupationalCredential",
        "credentialCategory": "Professional Designation",
        "name": "Certified Residential Specialist (CRS)"
      }
    ],
    "knowsAbout": [
      "Residential Real Estate",
      "First-Time Home Buyers",
      "Luxury Homes",
      "[Other specialties]"
    ],
    "knowsLanguage": ["en"],
    "award": [
      "[Award Name — Year]"
    ]
  },
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "[4.9]",
    "reviewCount": "[142]",
    "bestRating": "5",
    "worstRating": "1"
  },
  "review": [
    {
      "@type": "Review",
      "author": {
        "@type": "Person",
        "name": "[Reviewer Name or Initials]"
      },
      "reviewRating": {
        "@type": "Rating",
        "ratingValue": "5"
      },
      "reviewBody": "[Short testimonial text]"
    }
  ],
  "priceRange": "$$",
  "openingHours": "Mo-Fr 09:00-18:00",
  "sameAs": [
    "https://www.zillow.com/profile/[agent-id]",
    "https://www.linkedin.com/in/[agent-id]",
    "https://www.facebook.com/[agent-page]",
    "https://www.realtor.com/realestateagents/[agent-id]"
  ]
}
```

## How to Deliver Schema Markup

When generating schema markup for an agent:

1. **Collect all data points**: Name, address, phone, email, credentials, ratings, service areas, social profiles
2. **Generate the JSON-LD**: Fill in the template above with actual data
3. **Use placeholders for unknowns**: Mark missing data as `"[INSERT: your phone number]"` so the agent knows what to fill in
4. **Provide installation instructions**:

```html
<!-- Add this to the <head> section of your About/Bio page -->
<script type="application/ld+json">
[PASTE GENERATED JSON-LD HERE]
</script>
```

5. **Validate**: Recommend testing with Google's Rich Results Test (https://search.google.com/test/rich-results) and Schema.org Validator (https://validator.schema.org/)

## Supporting Schema Types

### BreadcrumbList (for navigation)
```json
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "itemListElement": [
    { "@type": "ListItem", "position": 1, "name": "Home", "item": "https://..." },
    { "@type": "ListItem", "position": 2, "name": "Our Agents", "item": "https://..." },
    { "@type": "ListItem", "position": 3, "name": "[Agent Name]" }
  ]
}
```

### FAQPage (for bio pages with Q&A sections)
```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "What areas does [Agent Name] serve?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "[Agent Name] serves [list of areas]."
      }
    },
    {
      "@type": "Question",
      "name": "What are [Agent Name]'s specialties?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "[Agent Name] specializes in [specialties]."
      }
    }
  ]
}
```

## Open Graph Meta Tags

In addition to JSON-LD, recommend these meta tags for social sharing and AI parsing:

```html
<meta property="og:title" content="[Agent Name] — REALTOR® in [City, State]" />
<meta property="og:description" content="[Short bio version]" />
<meta property="og:image" content="[Headshot URL]" />
<meta property="og:url" content="[Page URL]" />
<meta property="og:type" content="profile" />
<meta name="description" content="[Medium bio version, first 155 characters]" />
```

## Important Notes

- Only include data that is accurate and verifiable. Do not fabricate review counts or ratings.
- The `sameAs` array should link to all the agent's verified social/platform profiles — this helps AI engines confirm entity identity across the web.
- Update the markup whenever the bio is updated (new stats, new reviews, new awards).
- If the agent doesn't control their website's HTML, provide the markup and suggest they send it to their web developer or brokerage marketing team.
