# Peekaboo

> macOS vision tool — capture screen content, OCR text, and analyze what's on your screen.

**ClawHub:** https://clawhub.ai/steipete/peekaboo · ⭐ 51 · 936 installs  
**License:** MIT-0 · **API Key:** 🆓 Not required  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign)

---

## What It Does

Peekaboo is a macOS screen capture and OCR tool. It takes screenshots, extracts text using OCR, and lets your agent see what's on your screen. Useful for automation workflows that need to interact with GUI applications that don't have APIs.

## How to Install

```bash
clawhub install peekaboo
```

**Setup:** Grant screen recording permission to your terminal/agent environment in macOS System Settings > Privacy & Security > Screen Recording.

## Key Capabilities

- Take screenshots of the entire screen, specific windows, or regions
- OCR text from screenshots
- Analyze screen content for patterns or specific text
- Automate GUI workflows for apps without APIs
- No external dependencies beyond macOS built-in tools

## Usage Examples

**Extract text from screen:**
```
"Take a screenshot of the active window and extract all text from it"
```

**Find specific text on screen:**
```
"Check if the text 'Build Successful' appears on my screen anywhere"
```

**Automate GUI workflow:**
```
"Look at the Xcode window, find the 'Run' button, and tell me its position"
```

## Requirements

- **Binaries:** macOS built-in `screencapture` and OCR tools
- **API Keys:** None
- **Platform:** macOS only
- **Permissions:** Screen recording access required

## Tips & Gotchas

- Only works on macOS
- Screen recording permission must be granted first
- OCR accuracy varies depending on text quality and resolution
- For full GUI automation, pair with [Desktop Control](./desktop-control.md) (⚠️ high risk)

## Related Skills

- [Camsnap](./camsnap.md) — Camera capture complement to screen capture
- [Desktop Control](./desktop-control.md) — Full GUI automation (high risk)
