# Searxng

> Self-hosted meta-search engine integration. Privacy-focused, no tracking, no API keys required for self-hosted instances.

**ClawHub:** https://clawhub.ai/abk234/searxng · ⭐ 22 · 264 installs  
**License:** MIT-0 · **API Key:** 🆓 Not required for self-hosted instances  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign)

---

## What It Does

Searxng skill lets your agent query a self-hosted Searxng instance for private, untracked web searches. Perfect for privacy-focused users who run their own Searxng meta-search engine.

## How to Install

```bash
clawhub install searxng
```

**Setup:**
1. Run your own Searxng instance (https://docs.searxng.org/)
2. Set env var: `export SEARXNG_URL="https://your-searxng-instance.com"`

## Key Capabilities

- Private, untracked web searches
- No API keys required for self-hosted instances
- Aggregates results from multiple search engines
- No user tracking or data collection
- Customizable search filters and sources

## Usage Examples

**Basic search:**
```
"Search for 'openclaw skills' using my Searxng instance"
```

**Privacy-focused research:**
```
"Search for 'AI agent security best practices' with no tracking"
```

## Requirements

- **Binaries:** None
- **API Keys:** None (self-hosted)
- **Platform:** All
- **Prerequisite:** Self-hosted Searxng instance

## Tips & Gotchas

- You need to run your own Searxng instance to use this skill
- Public Searxng instances may have rate limits or be unreliable
- Searxng results are often lower quality than commercial search engines like Brave or Google
- Pair with [Multi Search Engine](./multi-search-engine.md) for broader search coverage

## Related Skills

- [Multi Search Engine](./multi-search-engine.md) — Broader search coverage with 17 engines
- [Brave Search](./brave-search.md) — Private commercial search alternative
