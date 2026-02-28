# Connectors

This plugin works standalone with web search and user-provided data. Enable optional MCP connectors for deeper integrations.

## Built-in

### Web Search
Used automatically for bio page audits, AI visibility scoring, and competitive analysis. No configuration needed.

## Optional Connectors

### Google Drive
Persist bio versions, profile trackers, and audit reports in Google Drive for cross-session access.

**Setup:**
1. Enable the Google Drive MCP connector in Claude's settings
2. Set `"disabled": false` for the `google-drive` entry in `.mcp.json`
3. Update the `"url"` field with your Google Drive MCP server endpoint

### Slack
Post optimized bios and audit reports to a team Slack channel for review and approval.

**Setup:**
1. Install the Slack MCP connector from the Claude plugin marketplace
2. Set `"disabled": false` for the `slack` entry in `.mcp.json`
3. Update the `"url"` field with your Slack MCP server endpoint

### Google Business Profile (Future)
Push bio description updates directly to Google Business Profile via the GBP API.

**Requirements:**
- A custom or community MCP server implementing the GBP API
- OAuth2 credentials with Business Profile Manager access
- Verified Google Business Profile listing

### Zillow (Future)
Sync bio content to Zillow agent profiles.

**Requirements:**
- A custom MCP server implementing Zillow API access (currently limited)
- Zillow Premier Agent account for API access

## Building Custom Connectors

If you want to build an MCP server for a real estate platform:

1. Check whether the platform has a public API
2. Review the [MCP specification](https://modelcontextprotocol.io/)
3. Implement the connector following MCP server best practices
4. Add the server URL to `.mcp.json` and submit a PR

Platforms most likely to support API-driven bio updates:
- Google Business Profile (has API, supports description updates)
- LinkedIn (limited API, "About" section may be writable for approved apps)
- WordPress-based brokerage sites (REST API for page/post content)
