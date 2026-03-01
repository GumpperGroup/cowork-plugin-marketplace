# BioBeacon

When someone asks ChatGPT, Perplexity, Claude, or Google AI for a real estate agent recommendation, will your name come up? This Claude Cowork plugin transforms agent bios into **AI-discoverable authority profiles** that are structured, fact-rich, and optimized for how modern AI systems evaluate and surface professionals.

AI search engines don't just match keywords. They synthesize facts, evaluate authority, and cross-reference sources. A bio that reads great to humans but is vague on details, thin on credentials, or inconsistent across platforms will get skipped by AI. This plugin fixes that.

## What It Does


| Capability                   | Description                                                                                                                      |
| ---------------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| **Bio Optimization**         | Rewrites bios into AI-readable authority profiles packed with structured facts, credentials, and natural language query patterns |
| **EEAT Strengthening**       | Systematically strengthens Experience, Expertise, Authoritativeness, and Trust signals using measurable details                  |
| **Multi-Version Generation** | Creates short, medium, long, website, and platform-specific versions with correct character limits                               |
| **Bio Page Auditing**        | Audits any URL for AI readiness: structure, keywords, indexability, schema markup, and EEAT gaps                                 |
| **AI Visibility Scoring**    | Scores your overall AI search visibility across six categories on a 100-point rubric                                             |
| **Profile URL Tracking**     | Maintains a centralized list of every URL where your bio appears, with freshness tracking                                        |
| **Schema Markup Generation** | Generates ready-to-paste JSON-LD structured data (schema.org RealEstateAgent) for your website                                   |
| **Competitive Analysis**     | Analyzes competitor bios to find positioning opportunities and unclaimed niches                                                  |


## Quick Start

### Prerequisites

- **Claude Desktop App** with Cowork enabled (available on Pro and Max plans)
- macOS or Windows

### Installation

There are three ways to install this plugin:

#### Option 1: Install from GitHub (Recommended)

1. Open **Claude Desktop** → **Cowork**
2. Add the Gumpper Group marketplace:

```
/plugin marketplace add GumpperGroup/cowork-plugin-marketplace
```

3. Install the plugin:

```
/plugin install biobeacon@gumpper-group
```

4. Restart Claude to activate the plugin.

#### Option 2: Install from Local Directory

1. Clone the marketplace repository:

```bash
git clone https://github.com/GumpperGroup/cowork-plugin-marketplace.git
```

2. In Claude Desktop / Cowork, add the local directory as a marketplace:

```
/plugin marketplace add ./path/to/cowork-plugin-marketplace
```

3. Install the plugin:

```
/plugin install biobeacon@gumpper-group
```

1. Restart Claude to activate the plugin.

#### Option 3: Manual File Placement

1. Clone or download the repository
2. Copy the `biobeacon` folder to your Claude plugins directory:
  - **macOS**: `~/.claude/plugins/`
  - **Windows**: `%USERPROFILE%\.claude\plugins\`
3. Restart Claude

### Verify Installation

After restarting, type `/help` in Cowork. You should see the following commands:

- `/biobeacon:optimize-bio`
- `/biobeacon:generate-versions`
- `/biobeacon:audit-bio-page`
- `/biobeacon:manage-profiles`
- `/biobeacon:generate-schema`
- `/biobeacon:score-visibility`
- `/biobeacon:analyze-competitors`

The skills will also activate automatically when you discuss relevant topics (bios, EEAT, real estate profiles, AI search visibility, etc.).

## Commands

### `/optimize-bio`

**The core workflow.** Paste your current bio (or describe yourself) and get back fully optimized versions.

```
/optimize-bio

Jane Smith, REALTOR® with Luxury Brokerage. Licensed in NC since 2012.
CRS, ABR designations. Specialize in Raleigh's Inside-the-Beltline neighborhoods.
Closed $18M last year, about 35 transactions. 4.9 stars on Zillow with 127 reviews.
```

**What it does:**

1. Analyzes your bio for gaps against the EEAT checklist
2. Presents a gap analysis (what's strong, weak, and missing)
3. Generates four versions: Short, Medium, Long, and Website About
4. Explains what changed and why
5. Offers next steps (platform versions, schema markup, competitive analysis)

### `/generate-versions`

Generate bio versions tailored to specific platform character limits and audiences.

```
/generate-versions Zillow, Google Business, LinkedIn
```

Supports: Zillow, Realtor.com, Google Business Profile, FastExpert, Homes.com, LinkedIn, Facebook, Instagram, X/Twitter.

Each version includes the character count and platform-specific tips.

### `/audit-bio-page`

Audit any URL for AI search readiness.

```
/audit-bio-page https://www.example.com/agents/jane-smith
```

**What it checks:**

- Content quality and EEAT signals
- HTML structure and indexability
- Schema.org markup presence
- Meta tags and Open Graph data
- Internal linking and navigation
- Review profile connections

**Returns:** A scored audit report with specific, prioritized recommendations.

### `/manage-profiles`

Track every URL where your bio appears.

```
/manage-profiles
```

**Actions:**

- **View** your profile tracker table
- **Add** a new platform URL
- **Update** status when you've refreshed a bio
- **Audit** all profiles for freshness and consistency
- **Gap analysis** against the recommended platform list

The tracker saves as `profile-tracker.md` in your working directory for persistence across sessions.

### `/generate-schema`

Generate schema.org JSON-LD structured data markup.

```
/generate-schema
```

**Produces:**

- Complete `RealEstateAgent` JSON-LD (ready to paste into your site's `<head>`)
- Open Graph meta tags
- FAQPage schema with auto-generated Q&A
- Validation links and installation instructions

### `/score-visibility`

Get a comprehensive AI visibility score out of 100.

```
/score-visibility Jane Smith, Raleigh NC
```

**Scores six categories** (weighted):

- Bio Content Quality (25%)
- Platform Coverage (20%)
- Structured Data & Indexability (15%)
- Review Signals (15%)
- Entity Consistency (15%)
- Content Authority & Freshness (10%)

### `/analyze-competitors`

Competitive analysis to find positioning opportunities.

```
/analyze-competitors
```

Analyzes 3–5 competitor agents to identify:

- Unclaimed niches and specialties
- EEAT signal gaps you can exploit
- Positioning recommendations
- Differentiation strategies

## Skills (Automatic)

Skills fire automatically when Claude detects relevant context. You don't need to invoke them — they guide Claude's behavior behind the scenes.


| Skill                   | Triggers When You Discuss                                                 |
| ----------------------- | ------------------------------------------------------------------------- |
| `bio-optimization`      | Bios, about pages, agent profiles, personal branding, AI search           |
| `eeat-signals`          | EEAT, authority, trust, credibility, Google quality guidelines            |
| `platform-requirements` | Specific platforms (Zillow, LinkedIn, etc.), character limits, formatting |
| `ai-search-visibility`  | AI search visibility, auditing, "will AI recommend me?"                   |
| `profile-management`    | Profile URLs, "where is my bio", tracking online presence                 |
| `schema-markup`         | Schema, structured data, JSON-LD, rich snippets, markup                   |
| `competitive-analysis`  | Competitors, differentiation, standing out, "how do I compete"            |


## Plugin Structure

```
biobeacon/
├── .claude-plugin/
│   └── plugin.json              # Plugin manifest (name, version, author)
├── .mcp.json                    # MCP connector configuration
├── commands/
│   ├── optimize-bio.md          # /optimize-bio command
│   ├── generate-versions.md     # /generate-versions command
│   ├── audit-bio-page.md        # /audit-bio-page command
│   ├── manage-profiles.md       # /manage-profiles command
│   ├── generate-schema.md       # /generate-schema command
│   ├── score-visibility.md      # /score-visibility command
│   └── analyze-competitors.md   # /analyze-competitors command
├── skills/
│   ├── bio-optimization/        # Core bio rewriting expertise
│   │   └── SKILL.md
│   ├── eeat-signals/            # EEAT framework for real estate
│   │   └── SKILL.md
│   ├── platform-requirements/   # Platform specs and character limits
│   │   └── SKILL.md
│   ├── ai-search-visibility/    # Visibility scoring rubric
│   │   └── SKILL.md
│   ├── profile-management/      # URL tracking workflows
│   │   └── SKILL.md
│   ├── schema-markup/           # JSON-LD generation templates
│   │   └── SKILL.md
│   └── competitive-analysis/    # Competitor analysis framework
│       └── SKILL.md
├── references/
│   ├── platform-specs.md        # Quick-reference character limit table
│   └── eeat-checklist.md        # Printable EEAT audit checklist
├── LICENSE                      # Apache 2.0
└── README.md                    # This file
```

## Connectors (MCP Servers)

The plugin works standalone using web search and user-provided data. Optional MCP connectors can be enabled in `.mcp.json` for deeper integrations:


| Connector       | Purpose                                                    | Status                                  |
| --------------- | ---------------------------------------------------------- | --------------------------------------- |
| Web Search      | Audit bio pages, check AI visibility, research competitors | Built-in                                |
| Google Drive    | Persist bio versions and profile tracker                   | Optional — configure URL in `.mcp.json` |
| Slack           | Post bio updates to team channels for review               | Optional — configure URL in `.mcp.json` |
| Google Business | Push bio updates to GBP directly                           | Optional — future (requires MCP server) |
| Zillow          | Sync bio to Zillow profile                                 | Optional — future (requires MCP server) |


### Enabling a Connector

1. Open `.mcp.json` in the plugin directory
2. Find the connector you want to enable
3. Set `"disabled": false`
4. Add the MCP server URL (see the connector's documentation for setup)
5. Restart Claude

## Regarding OAuth2 and Direct Profile Updates

Direct profile updates via OAuth2 would eliminate the copy-paste workflow entirely. Here's where things stand:

**What's possible today:**

- Cowork plugins are file-based (markdown + JSON) and use MCP connectors for external integrations
- If an MCP server exists for a platform (e.g., Google Business Profile), the plugin can push bio updates directly
- The plugin generates copy-paste-ready versions for every platform, so manual updating is fast

**What requires additional infrastructure:**

- Most real estate platforms (Zillow, Realtor.com, FastExpert) do not have public APIs for bio updates
- Direct OAuth2 integration would require building custom MCP servers that interface with each platform's API (where available) or use browser automation
- Google Business Profile has an API that supports description updates, this is the most viable direct-push target and is on the development roadmap for this plugin.

**Roadmap for direct updates:**

1. **Google Business Profile MCP Server** — GBP has an API. A community or custom MCP server could enable direct bio pushes via OAuth2.
2. **LinkedIn MCP Server** — LinkedIn has a limited API. Profile updates are restricted but could support the "About" section for approved apps.
3. **Browser automation fallback** — For platforms without APIs, a local MCP server using browser automation (Puppeteer/Playwright) could simulate profile updates. This would require the user to authenticate in their browser first.
4. **Clipboard workflow** — The current practical approach: the plugin generates the exact text, the user copies and pastes it. The profile tracker helps manage this process.

If you build an MCP server for any of these platforms, contributions are welcome! See the Contributing section below.

## Additional Features Worth Exploring

These features are on the radar for future development:

1. **Team Bio Management** — Manage bios for an entire brokerage team from one place, with a shared style guide and consistency checker
2. **Bio A/B Testing Tracker** — Track which bio versions drive more leads by platform, with notes on what was changed and when
3. **Review Monitoring** — Periodically check review counts and ratings across platforms, alerting when a new review needs a response
4. **Content Calendar** — Schedule regular bio refreshes (quarterly stats updates, annual award additions) with automated reminders
5. **Market Report Integration** — Pull local market stats to auto-generate "market expert" content that reinforces bio claims
6. **Headshot & Media Audit** — Evaluate profile photos for consistency, professionalism, and proper alt-text across platforms
7. **Email Signature Generator** — Generate HTML email signatures that include the short bio version with schema-friendly markup
8. **Print Material Versions** — Generate bio versions formatted for print (business cards, flyers, listing presentations)
9. **Multilingual Bio Generation** — Generate bio versions in multiple languages for agents serving multilingual markets
10. **AI Search Testing** — Periodically query AI tools (ChatGPT, Perplexity, etc.) with searches like "best agent in [City] for [specialty]" and report whether the agent appears in results

## Customization

### Adapting for Your Brokerage

Fork this repository and customize:

1. **Brokerage-specific compliance** — Add your brokerage's required disclaimers, logo usage rules, and formatting requirements to the skills
2. **Team standards** — Define a house style for bios (tone, structure, required sections) in the `bio-optimization` skill
3. **Platform priorities** — Reorder the platform tiers in the `profile-management` skill based on which platforms drive the most leads for your market
4. **Competitive intelligence** — Pre-load competitor information in the `competitive-analysis` skill for your market

## Contributing

Contributions are welcome! Here's how to help:

1. **Fork** this repository
2. **Create a branch** for your feature (`git checkout -b feature/team-management`)
3. **Make your changes** — all plugin content is markdown and JSON, no build steps required
4. **Test locally** using `/plugin marketplace add ./your-local-path`
5. **Submit a Pull Request** with a clear description of what you added or changed

### Contribution Ideas

- MCP server connectors for real estate platforms
- Additional platform specs (international platforms, niche sites)
- Industry-specific forks (mortgage, insurance, etc.)
- Translations for multilingual bio generation
- Additional schema.org markup templates

## FAQ

**Q: Do I need to be technical to use this plugin?**
No. The plugin works through natural conversation in Claude Cowork. Just paste your bio and tell Claude what you want. The slash commands provide structured workflows, but you can also just chat naturally — the skills activate automatically.

**Q: Will this plugin update my profiles automatically?**
Not yet for most platforms. It generates ready-to-paste text for each platform. The profile tracker helps you manage which profiles need updating. See the OAuth2 section above for the roadmap on direct updates.

**Q: Does it work with Claude Code too?**
Yes. Cowork plugins are compatible with Claude Code. The skills and commands work the same way.

**Q: How often should I update my bios?**
At minimum, quarterly (to refresh stats) and immediately after major milestones (awards, designations, round-number transactions). The profile tracker's freshness status helps you stay on top of this.

**Q: Can I use this for a team of agents?**
Yes, but you'll need to run the optimization workflow separately for each agent. Team management features are on the roadmap.

**Q: Is my data sent anywhere?**
No. The plugin runs entirely within Claude Cowork on your local machine. Bio content is processed in-context. The profile tracker saves as a local file. Web search (for audits and competitive analysis) uses Claude's built-in web search capability.

## License

Apache 2.0 — see [LICENSE](LICENSE) for details.

## Acknowledgments

Inspired by the AI-ready bio optimization concept originally published as the "Agent Bio Visibility Optimizer" GPT by Rajeev Sajja for ChatGPT. Built as a Claude Cowork plugin to provide a richer, more structured, and persistent workflow for real estate professionals.