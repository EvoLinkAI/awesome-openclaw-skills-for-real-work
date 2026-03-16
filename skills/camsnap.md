# Camsnap

> Take snapshots from your Mac's built-in camera or connected webcams.

**ClawHub:** https://clawhub.ai/steipete/camsnap · ⭐ 7 · 818 installs  
**License:** MIT-0 · **API Key:** 🆓 Not required  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign)

---

## What It Does

Camsnap lets your agent take still photos from your Mac's built-in iSight camera or any connected USB webcam. Extremely niche use case, mostly for security monitoring or automated photo capture workflows.

## How to Install

```bash
clawhub install camsnap
```

**Setup:** Grant camera access permissions to your terminal/agent environment in macOS System Settings > Privacy & Security > Camera.

## Key Capabilities

- Take photos from built-in or connected webcams
- Save photos to disk in JPG/PNG format
- Adjust resolution and quality settings
- Supports multiple cameras if connected
- No external dependencies beyond macOS built-in tools

## Usage Examples

**Take a photo:**
```
"Take a photo from my built-in camera and save it to ~/Pictures/cam.jpg"
```

**Take a photo with custom resolution:**
```
"Take a 1920x1080 photo from the external webcam and save it to security.jpg"
```

## Requirements

- **Binaries:** macOS built-in `imagesnap` tool (included with skill)
- **API Keys:** None
- **Platform:** macOS only
- **Permissions:** Camera access required

## Tips & Gotchas

- Only works on macOS
- Camera access permission must be granted first
- The green activity light will turn on when the camera is active — no silent capture possible on modern macOS
- For security monitoring, pair with [Proactive Agent](./proactive-agent.md) to take photos on motion detection

## Related Skills

- [Peekaboo](./peekaboo.md) — Screen capture skill, complement to camera capture
