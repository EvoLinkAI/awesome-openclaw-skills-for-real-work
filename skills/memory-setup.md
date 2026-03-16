# Memory Setup

> Transform your agent from goldfish to elephant — configure persistent MEMORY.md and vector search so your agent remembers everything between sessions.

**ClawHub:** https://clawhub.ai/jrbobbyhansen-pixel/memory-setup · ⭐ 83 · 238 installs  
**License:** MIT-0 · **API Key:** 🆓* (local provider available; Voyage/OpenAI optional)  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign, medium confidence)

---

## What It Does

Memory Setup is the foundational skill for giving your agent persistent memory. It configures OpenClaw's `memorySearch` feature, creates the workspace file structure (`MEMORY.md` + `memory/` directory), and explains how to initialize your agent's long-term context.

Without this (or equivalent setup), your agent starts fresh every session. With it, it remembers your preferences, project history, decisions, and past conversations.

**Start here before installing any other memory skill.**

## How to Install

```bash
clawhub install memory-setup
```

## Key Capabilities

- Configures `memorySearch` in OpenClaw/Clawdbot config
- Creates `MEMORY.md` and `memory/` directory structure
- Supports three embedding providers: Voyage AI, OpenAI, or local (no key)
- Indexes both `memory/` files and past session transcripts
- Troubleshooting guide for common setup failures
- AGENTS.md snippet for automatic memory recall behavior

## Setup Steps

**1. Enable in config (`~/.clawdbot/clawdbot.json`):**
```json
{
  "memorySearch": {
    "enabled": true,
    "provider": "voyage",
    "sources": ["memory", "sessions"],
    "indexMode": "hot",
    "minScore": 0.3,
    "maxResults": 20
  }
}
```

**2. Create workspace structure:**
```
workspace/
├── MEMORY.md              # Long-term curated memory
└── memory/
    ├── logs/              # Daily logs (YYYY-MM-DD.md)
    ├── projects/          # Project-specific context
    ├── groups/            # Group chat context
    └── system/            # Preferences, setup notes
```

**3. Initialize MEMORY.md:**
```markdown
# MEMORY.md — Long-Term Memory

## About [User Name]
- Key facts, preferences, context

## Active Projects
- Project summaries and status

## Decisions & Lessons
- Important choices made
- Lessons learned

## Preferences
- Communication style
- Tools and workflows
```

**4. Restart gateway:**
```bash
clawdbot gateway restart
```

## Provider Options

| Provider | Key Required | Notes |
|----------|-------------|-------|
| `voyage` | Yes — `VOYAGE_API_KEY` | Recommended quality |
| `openai` | Yes — `OPENAI_API_KEY` | Use `text-embedding-3-small` |
| `local` | ❌ None | No external API needed |

## Requirements

- **Binaries:** None
- **API Keys:** Optional — `VOYAGE_API_KEY` or `OPENAI_API_KEY` (use `local` provider for zero-key setup)
- **Platform:** All

## Tips & Gotchas

- Use `"provider": "local"` if you want zero external dependencies — quality is lower but fully private
- Lower `minScore` to `0.2` if memory search returns too few results
- MEMORY.md and daily logs contain personal data — treat them as sensitive, don't store secrets there
- If memory search isn't working after config changes, always restart the gateway first
- OpenAI provider config: use `"model": "text-embedding-3-small"` inside the memorySearch block

## Related Skills

- [Self-Improving + Proactive Agent](./self-improving-agent.md) — Builds on memory setup to auto-learn from corrections
- [Memory Manager](./memory-manager.md) — Advanced 3-tier semantic/episodic/procedural architecture
- [OpenClaw Backup](./openclaw-backup.md) — Back up your MEMORY.md and memory/ directory
