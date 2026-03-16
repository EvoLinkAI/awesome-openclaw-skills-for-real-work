# Summarize

> Fast CLI to summarize any URL, local file, or YouTube video — paste a link, get the key points. No browser needed.

**ClawHub:** https://clawhub.ai/steipete/summarize · ⭐ 634 · installs: N/A  
**License:** MIT-0 · **API Key:** 🔑 Required — one of: `OPENAI_API_KEY`, `ANTHROPIC_API_KEY`, `GEMINI_API_KEY`, or `XAI_API_KEY`  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign)

---

## What It Does

Summarize is a fast, flexible CLI that takes any URL, file path, or YouTube link and returns a concise summary. It handles web pages, PDFs, and YouTube videos (with transcript extraction). One of the most starred skills on ClawHub (⭐634) — it's a core utility that shows up in almost every workflow.

Default model is `google/gemini-3-flash-preview` — fast and cheap. Swap to stronger models for longer or more complex documents.

## How to Install

```bash
clawhub install summarize
```

## Key Capabilities

- Summarize any web URL — articles, docs, blog posts
- Summarize local files — PDFs, text, Markdown
- Summarize YouTube videos — transcript extraction (with optional Apify fallback)
- Adjustable length — short / medium / long / xl / xxl or custom character count
- JSON output for programmatic use
- Firecrawl fallback for paywalled or JavaScript-heavy sites
- Multiple AI provider support — OpenAI, Anthropic, Google, xAI

## Usage Examples

**Web article:**
```bash
summarize "https://example.com/article" --model google/gemini-3-flash-preview
```

**Local PDF:**
```bash
summarize "/path/to/document.pdf" --model google/gemini-3-flash-preview
```

**YouTube video:**
```bash
summarize "https://youtu.be/dQw4w9WgXcQ" --youtube auto
```

**Control output length:**
```bash
summarize "https://example.com" --length short    # Brief overview
summarize "https://example.com" --length xl        # Detailed
summarize "https://example.com" --length 500       # Exactly 500 chars
```

**JSON output (pipe to other tools):**
```bash
summarize "https://example.com" --json
```

**Extract content only (no summarization):**
```bash
summarize "https://example.com" --extract-only
```

## Config

Optional `~/.summarize/config.json` to set default model:
```json
{ "model": "openai/gpt-4o" }
```

## Requirements

- **Binaries:** None (npm package)
- **API Keys:** One of:
  - `OPENAI_API_KEY`
  - `ANTHROPIC_API_KEY`
  - `GEMINI_API_KEY` (aliases: `GOOGLE_GENERATIVE_AI_API_KEY`, `GOOGLE_API_KEY`)
  - `XAI_API_KEY`
- **Optional:** `FIRECRAWL_API_KEY` (for blocked sites), `APIFY_API_TOKEN` (YouTube fallback)
- **Platform:** All

## Tips & Gotchas

- Default model `google/gemini-3-flash-preview` is fast and cheap — use it for most things
- For YouTube, `--youtube auto` uses transcript; add `APIFY_API_TOKEN` for videos without transcripts
- For paywalled sites, set `--firecrawl always` with a Firecrawl key
- `--json` output works well when chaining with other tools or storing summaries in memory files
- Long documents benefit from `--length xl` or `--max-output-tokens 4096`

## Related Skills

- [Deep Research Pro](./deep-research-pro.md) — Multi-source research that uses summarization internally
- [Memory Setup](./memory-setup.md) — Store summaries in persistent memory
- [News Summary](./news-summary.md) — Automated daily news digest using summarization
- [YouTube Watcher](./youtube-watcher.md) — Deeper YouTube analysis beyond basic summarization
