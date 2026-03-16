# News Summary

> Automated daily news digest — get a concise summary of top news on the topics you care about, no scrolling required.

**ClawHub:** https://clawhub.ai/joargp/news-summary · ⭐ 78 · 238 installs  
**License:** MIT-0 · **API Key:** 🆓 Not required (uses free news APIs)  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign)

---

## What It Does

News Summary scrapes top news from multiple sources, filters it by topics you care about, and delivers a concise daily digest with key points and source links. No need to scroll through multiple news sites or social media — get the information that matters to you in one place.

## How to Install

```bash
clawhub install news-summary
```

## Key Capabilities

- Aggregate news from multiple sources (BBC, Reuters, TechCrunch, etc.)
- Filter news by custom topics: AI, tech, finance, politics, sports, etc.
- Generate concise summaries of each news item
- Include source links for full articles
- Schedule daily/weekly digests
- Avoid duplicate stories
- No API keys required for basic usage

## Usage Examples

**Get today's tech news:**
```
"Give me a summary of top AI and tech news from today"
```

**Custom topic digest:**
```
"Give me a digest of today's news about renewable energy and climate policy"
```

**Schedule daily digest:**
```
"Send me a daily news digest at 8am every weekday with tech, business, and world news"
```

**Specific source news:**
```
"Show me top news from TechCrunch and Hacker News from the past 24 hours"
```

## Requirements

- **Binaries:** `python3`, `requests`, `beautifulsoup4`
- **API Keys:** None (free tier usage; optional NewsAPI key for higher limits)
- **Platform:** All

## Tips & Gotchas

- For more reliable results, add a free NewsAPI key to unlock more sources and higher rate limits
- Customize your topic list to avoid irrelevant news
- Pair with [Summarize](./summarize.md) for deeper summaries of individual articles
- Use [Proactive Agent](./proactive-agent.md) to deliver digests automatically on schedule

## Related Skills

- [Summarize](./summarize.md) — Deep dive into individual articles
- [Proactive Agent](./proactive-agent.md) — Automated scheduled digests
- [Multi Search Engine](./multi-search-engine.md) — Search for specific news topics
