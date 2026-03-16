# Gemini

> Add Google Gemini as a model option to your agent — access Gemini 1.5 Pro, Gemini 1.5 Flash, and Gemini Advanced directly from chat.

**ClawHub:** https://clawhub.ai/steipete/gemini · ⭐ 44 · installs: N/A  
**License:** MIT-0 · **API Key:** 🔑 Required — `GEMINI_API_KEY` from Google AI Studio  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign)

---

## What It Does

Gemini skill adds Google's Gemini family of models as an option for your agent. Use Gemini 1.5 Flash (fast, cheap, 1M context window) for most tasks, Gemini 1.5 Pro for longer contexts, and Gemini Advanced for complex reasoning. Perfect for tasks where Google's models outperform OpenAI/Anthropic (multimodal, long contexts, creative work).

## How to Install

```bash
clawhub install gemini
```

**Setup:**
1. Get your API key from [Google AI Studio](https://aistudio.google.com/)
2. Set env var: `export GEMINI_API_KEY="your-key"`

## Key Capabilities

- Access all Gemini models: Gemini 1.5 Flash, Gemini 1.5 Pro, Gemini Advanced
- 1M+ token context window for long documents and codebases
- Multimodal support: process images, audio, video, and text
- Fast response times for most tasks
- Free tier available for low-volume usage
- Native multimodal support outperforms many other models

## Usage Examples

**Basic prompt:**
```
"[Gemini Flash] Explain quantum computing in simple terms"
```

**Long context task:**
```
"[Gemini Pro] Summarize this 100-page PDF and extract key action items"
```

**Multimodal task:**
```
"[Gemini Advanced] Describe this image and give me 3 design improvement suggestions"
```

**Code task:**
```
"[Gemini Flash] Write a Python script to parse CSV files and generate JSON output"
```

## Requirements

- **Binaries:** None
- **API Keys:** `GEMINI_API_KEY` — free tier available from [aistudio.google.com](https://aistudio.google.com/)
- **Platform:** All

## Tips & Gotchas

- Gemini 1.5 Flash is extremely fast and cheap — use it for most day-to-day tasks
- 1M context window lets you process entire codebases or books in one prompt
- Multimodal support is native and high quality — better than GPT-4o for some image/video tasks
- Free tier has rate limits — upgrade to paid for heavy usage
- Pair with [Free Ride](./free-ride.md) to automatically route appropriate tasks to Gemini

## Related Skills

- [Free Ride](./free-ride.md) — Auto-route tasks to Gemini when it's the best/cheapest option
- [Model Usage](./model-usage.md) — Track Gemini costs and usage
