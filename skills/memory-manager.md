# Memory Manager

> Professional 3-tier memory architecture (episodic/semantic/procedural) — never lose context, retrieve the right knowledge at the right time, survive context compression.

**ClawHub:** https://clawhub.ai/marmikcfc/memory-manager · ⭐ 68 · 159 installs  
**License:** MIT-0 · **API Key:** 🆓* (optional providers)  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign)

---

## What It Does

Memory Manager implements the cognitive science-inspired three-tier memory pattern used by leading agent systems: episodic (what happened), semantic (what I know), and procedural (how to do things). This structure outperforms flat vector retrieval by organizing knowledge the way humans actually think about it.

It includes scripts for initialization, compression risk detection, and automatic migration of flat memory files into the proper structure.

> Research basis: structured knowledge graphs beat flat vector retrieval by 18.5% (Zep team findings).

## How to Install

```bash
clawhub install memory-manager
```

## Key Capabilities

- **Three-tier architecture** — episodic/semantic/procedural, each stored separately
- **Compression risk detection** — warns before context window fills up (70% / 85% / critical thresholds)
- **Automatic migration** — converts flat `memory/*.md` into structured tiers
- **Snapshot/backup** — compresses and backs up memory before operations
- **Type-aware search** — query by memory type, not just keywords
- **Init script** — one command to set up the full structure

## Memory Architecture

| Tier | Files | Use For | Example Query |
|------|-------|---------|---------------|
| **Episodic** | `memory/episodic/YYYY-MM-DD.md` | Time-based events | "What did we decide last Tuesday?" |
| **Semantic** | `memory/semantic/topic.md` | Facts, knowledge, concepts | "What do I know about payment validation?" |
| **Procedural** | `memory/procedural/process.md` | Workflows, how-tos | "How do I deploy to staging?" |

## Usage Examples

**Initialize the structure:**
```bash
~/.openclaw/skills/memory-manager/init.sh
```

Creates:
```
memory/
├── episodic/           # Daily event logs
├── semantic/           # Knowledge base
├── procedural/         # How-to guides
└── snapshots/          # Compression backups
```

**Check context compression risk:**
```bash
~/.openclaw/skills/memory-manager/detect.sh
# ✅ Safe (<70% full)
# ⚠️ WARNING (70-85% full)
# 🚨 CRITICAL (>85% full)
```

**Migrate existing flat memory files:**
```bash
~/.openclaw/skills/memory-manager/organize.sh
# Automatically categorizes existing memory/*.md into episodic/semantic/procedural
```

## Requirements

- **Binaries:** `bash`
- **API Keys:** Optional (depends on underlying memory search provider)
- **Platform:** macOS · Linux

## Tips & Gotchas

- Run `detect.sh` before long tasks — context compression mid-task is disruptive
- The organize script categorizes by content heuristics — review the migration results manually
- Keep episodic logs chronological; don't backfill — accuracy matters for time-based queries
- Semantic files work best when focused on one topic per file (e.g., `payment-validation.md` not `backend.md`)
- Procedural files should be runnable step-by-step, not just descriptive notes

## Related Skills

- [Memory Setup](./memory-setup.md) — Basic memory config (prerequisite)
- [Self-Improving + Proactive Agent](./self-improving-agent.md) — Automatic learning layer on top of memory
- [OpenClaw Backup](./openclaw-backup.md) — Back up all memory tiers before major operations
