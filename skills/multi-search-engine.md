# Multi Search Engine

> 17 search engines in one skill — Google, Bing, DuckDuckGo, Brave, Baidu, WeChat, WolframAlpha, and more. No API keys. No limits.

**ClawHub:** https://clawhub.ai/gpyAngyoujun/multi-search-engine · ⭐ 297 · 766 installs  
**License:** MIT-0 · **API Key:** 🆓 Not required  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign)

---

## What It Does

Multi Search Engine gives your agent access to 17 search engines — 8 Chinese (Baidu, Bing CN, 360, Sogou, WeChat, Toutiao, Jisilu) and 9 international (Google, DuckDuckGo, Yahoo, Startpage, Brave, Ecosia, Qwant, WolframAlpha) — without any API keys. It uses `web_fetch` to query search engine result pages directly.

The best default search skill for new setups: works immediately, covers everything, and costs nothing. ⭐297 · 766 installs.

## How to Install

```bash
clawhub install multi-search-engine
```

## Key Capabilities

- 17 search engines across Chinese and international markets
- Advanced search operators (site:, filetype:, time filters, etc.)
- DuckDuckGo Bangs for site-specific shortcuts
- WolframAlpha for calculations and factual queries
- WeChat and Chinese social platform search
- No API keys, no rate limits from the skill itself

## Supported Engines

**International (9):**
- Google, Google HK, DuckDuckGo, Yahoo, Startpage, Brave, Ecosia, Qwant, WolframAlpha

**Chinese (8):**
- Baidu, Bing CN, Bing INT, 360, Sogou, WeChat, Toutiao, Jisilu

## Usage Examples

**Basic Google search:**
```javascript
web_fetch({"url": "https://www.google.com/search?q=python+async+tutorial"})
```

**Site-specific search:**
```javascript
web_fetch({"url": "https://www.google.com/search?q=site:github.com+react+hooks"})
```

**File type search:**
```javascript
web_fetch({"url": "https://www.google.com/search?q=machine+learning+filetype:pdf"})
```

**Past week only:**
```javascript
web_fetch({"url": "https://www.google.com/search?q=ai+news&tbs=qdr:w"})
```

**Privacy-first search:**
```javascript
web_fetch({"url": "https://duckduckgo.com/html/?q=privacy+tools"})
```

**DuckDuckGo Bang (jump to GitHub):**
```javascript
web_fetch({"url": "https://duckduckgo.com/html/?q=!gh+tensorflow"})
```

**WolframAlpha for calculations:**
```javascript
web_fetch({"url": "https://www.wolframalpha.com/input?i=100+USD+to+CNY"})
web_fetch({"url": "https://www.wolframalpha.com/input?i=distance+earth+to+moon"})
```

**Chinese WeChat content search:**
```javascript
web_fetch({"url": "https://wx.sogou.com/weixin?type=2&query=AI+agent"})
```

## Requirements

- **Binaries:** None
- **API Keys:** None
- **Platform:** All

## Tips & Gotchas

- Google results may vary by IP/region — use Google HK for different results
- WolframAlpha is uniquely useful for math, unit conversion, and factual lookups — not a general web search
- DuckDuckGo Bangs (`!gh` for GitHub, `!so` for Stack Overflow, `!npm` for npmjs) are extremely efficient
- For Chinese content, Baidu is more comprehensive; for Chinese social media, WeChat/Toutiao
- `web_fetch` parses HTML — results quality depends on the search engine's HTML structure staying stable
- For better result quality with API access, upgrade to [Brave Search](./brave-search.md)

## Related Skills

- [Brave Search](./brave-search.md) — Higher quality with API key
- [Deep Research Pro](./deep-research-pro.md) — Multi-source research using search as backbone
- [Exa Web Search](./exa-web-search.md) — Semantic search alternative
- [Baidu Web Search](https://clawhub.ai/ide-rea/baidu-search) — Dedicated Baidu skill for Chinese content
