# Exa Web Search (Free)

> Semantic neural web search — finds semantically relevant pages, not just keyword matches. No API key required for free tier.

**ClawHub:** https://clawhub.ai/Whiteknight07/exa-web-search-free · ⭐ 57 · 140 installs  
**License:** MIT-0 · **API Key:** 🆓 Free tier available (paid tier for higher limits)  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign)

---

## What It Does

Exa Web Search uses neural search technology to find pages that are semantically related to your query, not just pages that contain exact keyword matches. Perfect for research tasks where you want related content, not just literal matches. Free tier available with reasonable rate limits.

## How to Install

```bash
clawhub install exa-web-search-free
```

**Optional setup for higher limits:**
1. Get an API key from [exa.ai](https://exa.ai/)
2. Set env var: `export EXA_API_KEY="your-key"`

## Key Capabilities

- Semantic/neural search — understands context and meaning
- Finds pages related to your query even without exact keyword matches
- Full text content extraction for any URL
- Search recent content (past 24h, past week, etc.)
- Free tier available with no API key required
- Higher limits for paid tier users

## Usage Examples

**Semantic search:**
```
"Search for content related to 'agent memory architectures' — semantic matches, not just keyword"
```

**Recent content:**
```
"Find the latest research papers on multimodal agents from the past month"
```

**Extract content:**
```
"Get the full text content from https://example.com/research-paper"
```

**Combined search + content:**
```
"Find 5 semantically relevant pages about 'self-improving agents' and extract their full content"
```

## Requirements

- **Binaries:** None
- **API Keys:** Optional — `EXA_API_KEY` for higher rate limits
- **Platform:** All

## Tips & Gotchas

- Free tier has rate limits — upgrade to paid for heavy usage
- Semantic search works best for research and knowledge queries; use keyword search for factual lookups
- Exa has built-in content extraction — no need for separate scrapers
- Pair with [Deep Research Pro](./deep-research-pro.md) for multi-source research workflows

## Related Skills

- [Brave Search](./brave-search.md) — Keyword-based search alternative
- [Multi Search Engine](./multi-search-engine.md) — Zero-key search covering 17 engines
- [Deep Research Pro](./deep-research-pro.md) — Multi-source research workflow
