# Free Ride - Unlimited Free AI

> Route AI tasks to free tiers and open-source models automatically — reduce your AI costs by 70% or more.

**ClawHub:** https://clawhub.ai/Shaivpidadi/free-ride · ⭐ 274 · 247 installs  
**License:** MIT-0 · **API Key:** 🆓 Not required (works with your existing model keys)  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign)

---

## What It Does

Free Ride intelligently routes your AI tasks to the cheapest (or free) available model that can handle the task. Simple tasks go to free tiers or small local models, complex tasks go to paid models like GPT-4o or Claude 3 Opus only when necessary. Cut your AI costs drastically without sacrificing quality for most workloads.

⭐274 · 247 installs — one of the most popular cost-saving skills.

## How to Install

```bash
clawhub install free-ride
```

## Key Capabilities

- Automatic task routing based on complexity and requirements
- Supports all major model providers: OpenAI, Anthropic, Google, OpenRouter, local models
- Free tier detection: uses free tiers whenever possible
- Fallback routing: if a model is down or rate-limited, automatically try the next cheapest option
- Cost tracking and reporting: see how much you've saved
- Customizable routing rules: define your own priority order

## Usage Examples

**Send a task via Free Ride:**
```
"[Free Ride] Write a Python function to reverse a linked list"
# Automatically routes to a cheap/free model that can handle code tasks
```

**Complex task (routes to premium model):**
```
"[Free Ride] Design a scalable microservices architecture for a SaaS product with 1M users"
# Routes to Claude 3 Opus or GPT-4o for complex architecture work
```

**Cost report:**
```
"Show me how much I've saved with Free Ride this month"
```

**Custom routing rule:**
```
"Add a rule: all creative writing tasks go to Gemini Advanced first, then GPT-4o"
```

## Requirements

- **Binaries:** None
- **API Keys:** Your existing AI model API keys (OpenAI, Anthropic, Google, etc.)
- **Platform:** All

## Tips & Gotchas

- Simple tasks (code snippets, email writing, basic questions) can almost always be handled by free/cheap models
- You can override routing with `[Force Model: gpt-4o]` for critical tasks
- Local models are supported if you run them on your own hardware
- Pair with [Model Usage](./model-usage.md) to track costs and savings over time

## Related Skills

- [Model Usage](./model-usage.md) — Track per-model costs and usage
- [API Gateway](./api-gateway.md) — Manage API keys for multiple providers in one place
