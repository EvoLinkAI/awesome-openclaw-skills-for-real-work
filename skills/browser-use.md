# Browser Use

> Automate browser interactions: web testing, form filling, screenshots, data extraction. ⚠️ Security flagged.

**ClawHub:** https://clawhub.ai/ShawnPana/browser-use · ⭐ 65 · 265 installs  
**License:** MIT-0 · **API Key:** 🆓 Not required (uses Playwright/Puppeteer)  
**Security:** ⚠️ Flagged (OpenClaw: Suspicious patterns detected — review scan report before installing)

---

## What It Does

Browser Use lets your agent control a headless browser for web automation tasks: navigate websites, click elements, fill forms, take screenshots, extract data, and run web tests. It's a powerful tool for scraping and automation, but carries significant security risks.

> ⚠️ **Critical security warning:** ClawHub security scan flagged this skill as suspicious. It can be abused to access sensitive internal services, exfiltrate data, or perform malicious actions if misconfigured. Review the full scan report and source code before installing. Only run in a sandboxed environment with no access to internal networks.

## How to Install

```bash
# Review security scan first before installing
clawhub install browser-use
```

## Key Capabilities

- Full browser automation: navigate, click, type, submit forms
- Take full-page screenshots of any website
- Extract structured data from web pages
- Run end-to-end web tests
- Bypass basic anti-scraping measures
- Supports both Playwright and Puppeteer backends

## Usage Examples

**Scrape data from a website:**
```
"Go to https://example.com/products, extract all product names and prices, return as JSON"
```

**Fill a form:**
```
"Go to https://example.com/contact, fill out the form with my details, submit it"
```

**Take a screenshot:**
```
"Go to https://example.com/dashboard, take a full-page screenshot, save it to dashboard.png"
```

## Requirements

- **Binaries:** Playwright or Puppeteer, Node.js
- **API Keys:** None
- **Platform:** macOS · Linux · Windows

## Risks & Warnings

- ⚠️ Can be used to access internal services if running on a network with access to private resources
- ⚠️ Can execute arbitrary JavaScript in the browser context
- ⚠️ No built-in safeguards against malicious usage
- ⚠️ Only run in a sandboxed environment with restricted network access
- ⚠️ Never use with authenticated browser sessions that have access to sensitive accounts

## Alternatives

- [Agent Browser](./agent-browser.md) — Lower-risk maintained alternative
- [Playwright MCP](https://clawhub.ai/Spiceman161/playwright-mcp) — More secure MCP-based automation
