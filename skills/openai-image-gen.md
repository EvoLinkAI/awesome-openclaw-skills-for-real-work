# OpenAI Image Gen

> Generate images using OpenAI DALL-E 3 API directly from your agent.

**ClawHub:** https://clawhub.ai/steipete/openai-image-gen · ⭐ 24 · 857 installs  
**License:** MIT-0 · **API Key:** 🔑 Required — `OPENAI_API_KEY`  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign)

---

## What It Does

OpenAI Image Gen skill lets your agent generate images using OpenAI's DALL-E 3 API. Create high-quality images from text prompts, adjust size and quality, and download generated images directly. Perfect for designers, content creators, and anyone who needs quick visual assets.

## How to Install

```bash
clawhub install openai-image-gen
```

**Setup:**
1. Get your OpenAI API key from [platform.openai.com/api-keys](https://platform.openai.com/api-keys)
2. Set env var: `export OPENAI_API_KEY="your-key"`

## Key Capabilities

- Generate images using DALL-E 3
- Adjustable sizes: 1024x1024, 1792x1024, 1024x1792
- Adjustable quality: standard or HD
- Generate multiple variations of a prompt
- Download generated images directly to disk
- Support for detailed prompts and style specifications

## Usage Examples

**Generate an image:**
```
"Generate an image of a cyberpunk cat drinking coffee in a neon Tokyo alley, 8k, photorealistic style, 1792x1024 HD quality"
```

**Generate variations:**
```
"Generate 3 variations of this image prompt: 'minimalist logo for an AI agent company, blue and purple color scheme'"
```

## Requirements

- **Binaries:** None (API-based)
- **API Keys:** `OPENAI_API_KEY`
- **Platform:** All

## Tips & Gotchas

- DALL-E 3 pricing: $0.04 per 1024x1024 standard image, $0.08 per HD image
- Be specific in prompts for best results: include style, lighting, resolution, and color scheme
- Generated images are owned by you (per OpenAI terms)
- Pair with [SuperDesign](https://clawhub.ai/mpociot/superdesign) for design feedback on generated images

## Related Skills

- [SuperDesign](https://clawhub.ai/mpociot/superdesign) — Design feedback and improvement suggestions
