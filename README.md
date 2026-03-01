# Gumpper Group Plugin Marketplace

A private [Claude Cowork / Claude Code plugin marketplace](https://docs.claude.com) maintained by Gumpper Group, LLC.

## Available Plugins

| Plugin | Description |
| --- | --- |
| **[biobeacon](./plugins/biobeacon/)** | Optimize real estate agent bios for AI-driven search engines. Generate EEAT-optimized, platform-specific bio versions, audit bio pages, track profiles, and generate structured data markup. |

## Installation

### 1. Add the Marketplace

In Claude Desktop / Cowork or Claude Code, run:

```
/plugin marketplace add GumpperGroup/cowork-plugin-marketplace
```

### 2. Install a Plugin

```
/plugin install biobeacon@gumpper-group
```

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
