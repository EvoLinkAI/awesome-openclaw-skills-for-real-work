# Deep Research Pro

> Multi-source research agent — breaks any topic into sub-questions, searches 15-30 sources, deep-reads key pages, and delivers a structured cited report. No API keys.

**ClawHub:** https://clawhub.ai/parags/deep-research-pro · ⭐ 45 · 187 installs  
**License:** MIT-0 · **API Key:** 🆓 Not required (uses DuckDuckGo)  
**Security:** ⚠️ Flagged (OpenClaw: Suspicious, medium confidence — depends on external DDG script; review before use)

---

## What It Does

Deep Research Pro turns your agent into a systematic researcher. Give it any topic and it breaks it down into 3-5 sub-questions, runs multiple web and news searches per sub-question, deep-reads the most promising sources, and synthesizes everything into a structured report with inline citations.

The output is a proper research document — executive summary, thematic sections, key takeaways, source list, and methodology. Saved to `~/clawd/research/[slug]/report.md`.

> ⚠️ **Security note:** The skill depends on a DDG search script at `/home/clawdbot/clawd/skills/ddg-search/scripts/ddg` and uses `curl` + `python3` to fetch URLs. OpenClaw flagged it as suspicious (medium confidence) due to broad URL fetching and sub-agent spawning. Review the ddg-search dependency before installing.

## How to Install

```bash
clawhub install deep-research-pro
```

**Prerequisite:** The `ddg-search` skill must be installed first:
```bash
clawhub install ddg-search
```

## Key Capabilities

- Breaks topics into 3-5 research sub-questions
- Runs 2-3 keyword variations per sub-question (web + news)
- Targets 15-30 unique sources per report
- Deep-reads 3-5 key sources in full (not just snippets)
- Structured report: executive summary, themes, takeaways, sources, methodology
- Prioritizes: academic/official > reputable news > blogs > forums
- Flags unverified claims (single-source) and knowledge gaps
- Saves report as Markdown to `~/clawd/research/[slug]/report.md`

## Report Structure

```markdown
# [Topic]: Deep Research Report
*Generated: [date] | Sources: [N] | Confidence: [High/Medium/Low]*

## Executive Summary
[3-5 sentence overview]

## 1. [First Major Theme]
- Key point ([Source Name](url))
- Supporting data ([Source Name](url))

## Key Takeaways
- [Actionable insight 1]

## Sources
1. [Title](url) — [one-line summary]

## Methodology
Searched [N] queries across web and news. Analyzed [M] sources.
```

## Usage Examples

```
"Research the current state of nuclear fusion energy"
"Deep dive into Rust vs Go for backend services in 2026"
"Research the best strategies for bootstrapping a SaaS business"
"What's happening with the US housing market right now?"
```

## Requirements

- **Binaries:** `curl`, `python3`, DDG search script
- **API Keys:** None
- **Dependencies:** `ddg-search` skill
- **Platform:** Linux (script paths use `/home/clawdbot/...`)

## Tips & Gotchas

- If the DDG script path doesn't exist, the skill will fail silently — verify `ddg-search` is installed first
- The skill fetches arbitrary URLs with curl — don't run in environments with access to internal services
- Sub-agent spawning (`sessions_spawn`) is used for long research — check your platform's sub-agent policies
- Report files saved to `~/clawd/research/` — verify that path is acceptable before running
- Say "just research it" to skip the clarifying questions and use defaults

## Related Skills

- [Brave Search](./brave-search.md) — Higher-quality search with API key (good Brave alternative to DDG)
- [Summarize](./summarize.md) — Summarize individual sources before synthesizing
- [Memory Setup](./memory-setup.md) — Store research findings in persistent memory
