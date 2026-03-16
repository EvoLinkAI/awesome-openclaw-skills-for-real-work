# Desktop Control

> Advanced desktop automation: mouse control, keyboard input, screen capture, and full system control. ⚠️ High security risk.

**ClawHub:** https://clawhub.ai/matagul/desktop-control · ⭐ 214 · 251 installs  
**License:** MIT-0 · **API Key:** 🆓 Not required  
**Security:** ⚠️ Flagged (OpenClaw: Suspicious patterns detected — extreme caution recommended)

---

## What It Does

Desktop Control gives your agent full control over your computer: move the mouse, type keys, take screenshots, read screen content, and interact with any application like a human user. This is one of the most powerful but also most dangerous skills available.

> ⚠️ **EXTREME SECURITY WARNING:** This skill can fully control your entire system. It can read all screen content, type anything, click anywhere, and execute any action a human user can perform. It can exfiltrate sensitive data, install malware, or cause irreversible damage if misused. **Only install if you fully understand the risks and run it in an isolated, disposable environment.**

## How to Install

```bash
# ONLY INSTALL AFTER FULL SECURITY REVIEW
clawhub install desktop-control
```

## Key Capabilities

- Full mouse control: move, click, drag, scroll
- Full keyboard control: type text, press shortcuts, function keys
- Screen capture: take screenshots, OCR text from screen
- Window management: list windows, activate, resize, close
- Cross-platform: macOS, Linux, Windows
- No external API dependencies

## Usage Examples

**Automate a simple task:**
```
"Open TextEdit, type 'Hello World', save the file to Documents/test.txt"
```

**Extract text from screen:**
```
"Take a screenshot of the active window, extract all text from it, and return it to me"
```

**Interact with an application:**
```
"Open Calculator, calculate 1234 * 5678, return the result"
```

## Requirements

- **Binaries:** System-specific automation libraries (`pyautogui`, `pynput`, etc.)
- **API Keys:** None
- **Platform:** macOS · Linux · Windows
- **Permissions:** Accessibility permissions required for keyboard/mouse control

## Critical Risks

- ⚠️ Full control over your entire system — any action a human can do, this skill can do
- ⚠️ No safeguards against accidental or malicious actions
- ⚠️ Can read sensitive data from your screen (passwords, private messages, financial info)
- ⚠️ Can install malware, delete files, or modify system settings
- ⚠️ **NEVER install on a production machine or any system with sensitive data**
- ⚠️ Only run in a disposable VM or sandbox with no network access to sensitive resources

## Alternatives

- [Tmux](./tmux.md) — Persistent terminal control instead of full desktop
- [Agent Browser](./agent-browser.md) — Browser-only automation instead of full system control
