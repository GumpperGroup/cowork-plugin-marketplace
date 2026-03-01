# Gumpper Group Plugin Marketplace

A private [Claude Cowork / Claude Code plugin marketplace](https://docs.claude.com) maintained by Gumpper Group, LLC.

## Available Plugins

| Plugin | Description |
| --- | --- |
| **[biobeacon](./plugins/biobeacon/)** | Optimize real estate agent bios for AI-driven search engines. Generate EEAT-optimized, platform-specific bio versions, audit bio pages, track profiles, and generate structured data markup. |

## Installation

### 1. Open the Plugin Manager

1. In **Claude Desktop → Cowork**, click the **+** (plus) button
2. Select **"Plugins"**
3. Select **"Add Plugins"**

### 2. Add the Marketplace

1. On the Plugins page, select the **"Personal"** tab
2. Click the **+** (plus) button
3. Enter the marketplace owner/repo: `gumpper-group/biobeacon`

### 3. Restart Claude

Restart Claude to activate the plugin.

## Adding New Plugins

To add a new plugin to this marketplace:

1. Create a new directory under `plugins/` with your plugin's kebab-case name
2. Include a `.claude-plugin/plugin.json` manifest inside the plugin directory
3. Add the plugin entry to `.claude-plugin/marketplace.json`
4. Commit and push

## Marketplace Structure

```
cowork-plugin-marketplace/
├── .claude-plugin/
│   └── marketplace.json         # Marketplace catalog
├── plugins/
│   ├── biobeacon/               # BioBeacon plugin
│   │   ├── .claude-plugin/
│   │   │   └── plugin.json
│   │   ├── commands/
│   │   ├── skills/
│   │   ├── references/
│   │   ├── .mcp.json
│   │   └── CONNECTORS.md
│   └── (future plugins go here)
└── README.md
```

## License

Apache 2.0 — see [LICENSE](LICENSE) for details.
