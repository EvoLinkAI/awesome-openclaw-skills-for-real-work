# Proactive Agent

> Your agent stops waiting and starts anticipating — monitors what matters, initiates check-ins, survives context compression, and self-improves with guardrails.

**ClawHub:** https://clawhub.ai/halthelobster/proactive-agent · ⭐ 557 · installs: N/A  
**License:** MIT-0 · **API Key:** 🆓 Not required  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign)

---

## What It Does

Proactive Agent (by Hal Labs, v3.1.0) is a full behavioral architecture for your agent — not just a skill, but a set of principles and protocols that change how it operates. The three pillars: **Proactive** (asks "what would help my human?" instead of waiting), **Persistent** (survives context compression with WAL protocol and Working Buffer), and **Self-improving** (evolves with guardrails that prevent drift).

⭐557 — one of the highest-starred skills on ClawHub. Works best alongside [Self-Improving + Proactive Agent](./self-improving-agent.md).

## How to Install

```bash
clawhub install proactive-agent
```

## Key Capabilities

**Proactive:**
- Anticipates needs — reverse prompting surfaces ideas you didn't know to ask for
- Proactive check-ins — monitors what matters and reaches out when needed
- "What would help my human?" mindset instead of wait-and-respond

**Persistent (context-survival):**
- WAL Protocol — writes critical details BEFORE responding, never after
- Working Buffer — captures every exchange in the danger zone before compaction
- Compaction Recovery — step-by-step recovery when context gets truncated
- Unified Search — checks all sources before saying "I don't know"

**Self-improving:**
- Relentless resourcefulness — tries 10 approaches before giving up or asking
- Self-healing — fixes its own issues autonomously
- Safe evolution with ADL/VFM protocols — prevents drift and complexity creep
- Knows when to use `systemEvent` vs `isolated agentTurn` crons (v3.1.0)

**Security:**
- Skill installation vetting built-in
- Agent network warnings
- Context leakage prevention

## Usage Examples

The skill changes agent **behavior** rather than providing explicit commands. After installing, your agent will:

```
# Instead of waiting for you to ask:
"I noticed you've been working on the auth refactor for 3 days —
want me to draft a summary of what's been completed?"

# Instead of giving up:
"Let me try 3 more approaches before I ask you for help..."

# Instead of losing context after compaction:
"[Recovering from context loss — checking WAL and Working Buffer...]
I was in the middle of [task]. Here's where we left off..."
```

## What Changed in v3.1.0

- **Autonomous vs Prompted Crons** — understands when `systemEvent` (main session) vs `isolated agentTurn` (background) is appropriate
- **Verify Implementation, Not Intent** — checks that mechanisms actually work, not just that instructions exist
- **Tool Migration Checklist** — when deprecating tools, updates ALL references automatically

## Requirements

- **Binaries:** None
- **API Keys:** None
- **Platform:** All

## Tips & Gotchas

- This skill is a behavioral overlay — it affects everything your agent does, not just specific commands
- Pair with [Self-Improving + Proactive Agent](./self-improving-agent.md) for the strongest combination
- Review the skill's boundaries documentation — proactivity without guardrails can be annoying
- The WAL protocol means your agent writes to files frequently — ensure disk space and permissions
- For lighter-weight proactivity, see [Proactive Agent Lite](https://clawhub.ai/BestRocky/proactive-agent-lite)

## Related Skills

- [Self-Improving + Proactive Agent](./self-improving-agent.md) — The most natural companion skill
- [Memory Setup](./memory-setup.md) — Required for context persistence
- [Memory Manager](./memory-manager.md) — Advanced memory for the WAL protocol to write to
