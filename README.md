# DevEx Marketplace

Afya DevEx Marketplace — a collection of skills, plugins, workflows, and productivity tools for software developers using Claude Code, Cursor, and GitHub Copilot.

Built by Afya's Developer Experience (DevEx) team.

## Installation

### Claude Code

Add this marketplace to Claude Code:

```bash
/plugin marketplace add iclinic/devex-marketplace
```

### Cursor

1. Go to the [Cursor Plugin Dashboard](https://cursor.com/dashboard/plugins)
2. Import `iclinic/devex-marketplace` as a team marketplace

To install a plugin, click on it in the dashboard and then click **Add to Cursor** to install it directly from the Cursor desktop IDE.

### GitHub Copilot

Add this marketplace to GitHub Copilot:

```bash
copilot plugin marketplace add iclinic/devex-marketplace
```

## Available Plugins

### Afyapowers (Core)

A deterministic, phase-gated development workflow plugin forked from superpowers. Enforces structured feature development with persistent state, session continuity, and full auditability.

**Install:**

| Platform | Command |
|---|---|
| Claude Code | `/plugin install afyapowers@devex-marketplace` |
| Cursor | Install via the [Cursor Plugin Dashboard](https://cursor.com/dashboard/plugins) |
| GitHub Copilot | `copilot plugin install afyapowers@devex-marketplace` |

**What you get:**
- Structured, phase-gated development workflow
- Persistent state and session continuity
- Full auditability for feature development

**Repository:** https://github.com/iclinic/afyapowers

---

## Project Structure

```
devex-marketplace/
├── .claude-plugin/
│   └── marketplace.json       # Claude Code plugin catalog
├── .cursor-plugin/
│   └── marketplace.json       # Cursor plugin catalog
├── .github/
│   └── plugin/
│       └── marketplace.json   # GitHub Copilot plugin catalog
└── README.md
```

## Contributing

To add a new plugin to the marketplace, add the plugin definition to all three marketplace files:

- `.claude-plugin/marketplace.json`
- `.cursor-plugin/marketplace.json`
- `.github/plugin/marketplace.json`

Each platform has a slightly different source format. See existing entries for reference.

## License

Internal use — Afya.
