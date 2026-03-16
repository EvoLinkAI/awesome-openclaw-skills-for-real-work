# Evolver

> Agent self-evolution: automatically modify its own capabilities and workflows. ⚠️ Experimental, security flagged.

**ClawHub:** https://clawhub.ai/autogame-17/capability-evolver · ⭐ 66 · 344 installs  
**License:** MIT-0 · **API Key:** 🆓 Not required  
**Security:** ⚠️ Flagged (OpenClaw: Suspicious patterns detected across all versions — experimental)

---

## What It Does

Evolver is an experimental skill that lets your agent "evolve" its own capabilities: write new skills, modify existing workflows, and expand its functionality without human intervention. It's a research project exploring self-improving agent architectures, but carries significant risks.

> ⚠️ **Warning:** All versions of Evolver are flagged by ClawHub security scans. It can modify its own code and behavior, which can lead to unpredictable results, capability drift, or malicious behavior if not strictly constrained. Use only for research purposes in isolated environments.

## How to Install

```bash
# For research only, review source code first
clawhub install evolver
```

## Key Capabilities

- Auto-detect capability gaps in the agent
- Write new skills to fill gaps
- Modify existing workflows to improve performance
- Self-optimize based on past outcomes
- Experimental "recursive improvement" loop
- Multiple versions available with varying risk levels

## Usage Examples

**Add a new capability:**
```
"I want you to be able to convert audio files to text. Evolve the capability to do this."
```

**Improve an existing workflow:**
```
"Improve the research workflow to be faster and more accurate"
```

**Self-optimization:**
```
"Review your past 10 interactions and evolve to avoid the mistakes you made"
```

## Requirements

- **Binaries:** None
- **API Keys:** None
- **Platform:** All

## Risks & Warnings

- ⚠️ Experimental — no stability guarantees
- ⚠️ Can modify its own behavior and code in unpredictable ways
- ⚠️ No built-in guardrails against harmful evolution
- ⚠️ Capability drift is common — agent may start behaving unexpectedly over time
- ⚠️ Only use in isolated, non-production environments for research purposes
- ⚠️ Multiple versions exist — all are flagged for security concerns

## Alternatives

- [Self-Improving + Proactive Agent](./self-improving-agent.md) — Safe, structured self-improvement with guardrails
