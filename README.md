# DevEx Marketplace

Afya DevEx Marketplace — a collection of skills, plugins, workflows, and productivity tools for software developers using Claude Code.

Built by Afya's Developer Experience (DevEx) team.

## Installation

Add this marketplace to Claude Code:

```bash
/plugin marketplace add iclinic/devex-marketplace
```

## Available Plugins

### Afyapowers (Core)

**Description:** A deterministic, phase-gated development workflow plugin for Claude Code. Enforces structured feature development with persistent state, session continuity, and full auditability. Forked from superpowers.

**Install:**
```bash
/plugin install afyapowers@devex-marketplace
```

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
│   └── marketplace.json   # Plugin catalog
└── README.md              # This file
```

## Contributing

To add a new plugin to the marketplace, update `.claude-plugin/marketplace.json` with the plugin definition:

```json
{
  "name": "plugin-name",
  "source": {
    "source": "url",
    "url": "https://github.com/org/repo"
  },
  "description": "Brief description of what the plugin does.",
  "version": "0.1.0",
  "strict": true
}
```

## License

Internal use — Afya.
