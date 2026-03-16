# Self-Improving + Proactive Agent

> Your agent learns from every correction permanently — builds tiered memory, self-reflects, and gets better at serving you over time. No credentials needed.

**ClawHub:** https://clawhub.ai/ivangdavila/self-improving · ⭐ 384 · 902 installs  
**License:** MIT-0 · **API Key:** 🆓 Not required  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign, high confidence)

---

## What It Does

This is the most impactful single skill in the OpenClaw ecosystem. It gives your agent a structured local memory that persists between sessions, automatically captures corrections and preferences, and self-reflects after significant work to improve future behavior.

The architecture uses tiered storage: a HOT tier (≤100 lines, always loaded), WARM tier (project/domain-specific, loaded on demand), and COLD archive. Patterns automatically promote and demote based on usage frequency — no manual curation required.

⭐ 384 · 902 installs — one of the most-installed skills on ClawHub.

## How to Install

```bash
clawhub install self-improving
```

## Key Capabilities

- **Automatic correction capture** — detects "No, that's wrong" / "I told you before" / "Stop doing X" and logs them
- **Preference learning** — picks up "I like when you..." / "Always do X for me" patterns
- **Tiered memory** — HOT (always loaded), WARM (on-demand), COLD (archived)
- **Auto-promotion/demotion** — patterns used 3x in 7 days → HOT; unused 30 days → WARM; unused 90 days → COLD
- **Self-reflection** — after completing significant work, evaluates outcome vs intent
- **Heartbeat maintenance** — keeps memory organized in the background
- **Full transparency** — cites memory source on every use; weekly digests available; full export on demand
- **Kill switch** — wipe all learned data with confirmation

## Memory Structure

```
~/self-improving/
├── memory.md          # HOT: ≤100 lines, always loaded
├── index.md           # Topic index with line counts
├── heartbeat-state.md # Heartbeat state
├── projects/          # Per-project learnings
├── domains/           # Domain-specific (code, writing, comms)
├── archive/           # COLD: decayed patterns
└── corrections.md     # Last 50 corrections log
```

## Learning Signals (Auto-Detected)

**Corrections → logged immediately:**
- "No, that's not right..."
- "Actually, it should be..."
- "I prefer X, not Y"
- "Remember that I always..."
- "Stop doing X"

**Preference signals → added to memory if explicit:**
- "I like when you..."
- "Always do X for me"
- "My style is..."

**Pattern candidates → promoted after 3x repetition:**
- Same instruction repeated 3+ times
- Workflow that works well repeatedly

**Ignored (not logged):**
- One-time instructions ("do X now")
- Context-specific ("in this file...")
- Hypotheticals ("what if...")

## Usage Examples

**Check what the agent has learned:**
```
"What do you know about my coding preferences?"
"Show my patterns"
"Memory stats"
```

**Query memory:**
```
"What have you learned about how I handle deployments?"
"Show [project] patterns"
```

**Manage memory:**
```
"Forget X"        # Remove with confirmation
"Export memory"   # ZIP all files
```

## Requirements

- **Binaries:** None
- **API Keys:** None
- **Platform:** macOS · Linux · Windows
- **Optional:** `Proactivity` companion skill (requires network access to install)

## Tips & Gotchas

- Back up `AGENTS.md` and `SOUL.md` before installing — the skill may make non-destructive edits to these files
- Memory is scoped: project patterns stay in `projects/{name}.md`, global in HOT tier — they don't leak across projects
- When patterns conflict, most specific wins: project > domain > global; most recent wins at same level
- The skill explicitly NEVER reads files outside `~/self-improving/` and NEVER modifies its own SKILL.md
- Test the kill-switch (`"wipe all memory"`) on a test setup before relying on it in production
- Review `boundaries.md` inside the skill — it documents what it will and won't store

## Related Skills

- [Memory Setup](./memory-setup.md) — Foundation memory config (set this up first)
- [Memory Manager](./memory-manager.md) — More advanced 3-tier memory architecture
- [Proactive Agent](./proactive-agent.md) — Adds proactive check-ins and anticipatory behavior
