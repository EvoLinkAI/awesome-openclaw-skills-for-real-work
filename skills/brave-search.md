# Brave Search

> Fast, private web search and full page content extraction via Brave Search API — no browser, no JavaScript overhead, clean Markdown output.

**ClawHub:** https://clawhub.ai/steipete/brave-search · ⭐ 149 · 529 installs  
**License:** MIT-0 · **API Key:** 🔑 Required — `BRAVE_API_KEY` from [brave.com/search/api](https://brave.com/search/api/)  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign)

---

## What It Does

Brave Search gives your agent fast, high-quality web search results and the ability to extract full page content as clean Markdown — all without launching a browser. The Brave Search API has excellent signal-to-noise ratio (no ad-stuffed SEO spam), making it one of the better search backends for agents.

⭐149 · 529 installs — the go-to search skill for users who want API-grade results.

## How to Install

```bash
clawhub install brave-search
```

**Setup:**
```bash
cd ~/Projects/agent-scripts/skills/brave-search
npm ci
export BRAVE_API_KEY="your-key"  # Get free key at brave.com/search/api
```

## Key Capabilities

- Web search with configurable result count
- Full page content extraction as Markdown (any URL)
- Combined search + content fetch in one call
- No browser required — pure API calls
- Clean output format for agent consumption

## Usage Examples

**Basic search (5 results):**
```bash
./search.js "rust async runtime comparison 2026"
```

**More results:**
```bash
./search.js "openai api pricing" -n 10
```

**Search + fetch page content:**
```bash
./search.js "react server components guide" -n 3 --content
```

**Extract content from a specific URL:**
```bash
./content.js https://docs.rust-lang.org/book/ch16-00-concurrency.html
```

**Output format:**
```
--- Result 1 ---
Title: Page Title
Link: https://example.com/page
Snippet: Description from search results
Content: (if --content flag used)
  Markdown content extracted from the page...
```

## Requirements

- **Binaries:** `node`, `npm`
- **API Keys:** `BRAVE_API_KEY` — free tier available at [brave.com/search/api](https://brave.com/search/api/)
- **Platform:** macOS · Linux · Windows

## Tips & Gotchas

- Free tier: 2,000 queries/month — more than enough for personal agent use
- `--content` flag extracts full page text — useful for going beyond snippets for key sources
- `./content.js` is separate from search — use it to fetch any specific URL directly
- Brave's index tends to have better technical content than Google for developer queries
- Combine with [Summarize](./summarize.md) for deep page analysis after finding relevant URLs

## Related Skills

- [Multi Search Engine](./multi-search-engine.md) — Zero-API-key alternative covering 17 engines
- [Deep Research Pro](./deep-research-pro.md) — Multi-source research workflow using search as backbone
- [Exa Web Search](./exa-web-search.md) — Semantic/neural search alternative
- [Summarize](./summarize.md) — Summarize pages found via search
