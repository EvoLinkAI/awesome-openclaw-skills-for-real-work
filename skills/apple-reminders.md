# Apple Reminders

> Manage Apple Reminders directly from your agent — create tasks, set due dates, get reminders, sync across all Apple devices.

**ClawHub:** https://clawhub.ai/steipete/apple-reminders · ⭐ 39 · 885 installs  
**License:** MIT-0 · **API Key:** 🆓 Not required (uses macOS native AppleScript)  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign)

> Note: There are 4 duplicate versions of this skill on ClawHub — this is the main stable version.

---

## What It Does

Apple Reminders skill lets your agent manage your Apple Reminders on macOS. Create tasks, set due dates, priorities, and lists, mark tasks as complete, and get reminders. Syncs automatically across all your Apple devices via iCloud. Perfect for macOS/iOS users who use Apple Reminders as their task management tool.

## How to Install

```bash
clawhub install apple-reminders
```

**Setup:** Grant automation permission to your terminal/agent environment in macOS System Settings > Privacy & Security > Automation.

## Key Capabilities

- Create new reminders with title, due date, priority, and list
- Mark reminders as complete/incomplete
- List reminders by list, due date, or priority
- Delete reminders
- Syncs automatically across all Apple devices via iCloud
- No external API dependencies

## Usage Examples

**Create a new reminder:**
```
"Create a reminder: 'Finish awesome-openclaw-skills README' due tomorrow at 5pm, priority 1, in the 'Work' list"
```

**List today's reminders:**
```
"Show me all reminders due today"
```

**Mark a reminder as complete:**
```
"Mark the 'Finish skill docs' reminder as complete"
```

## Requirements

- **Binaries:** macOS built-in AppleScript
- **API Keys:** None
- **Platform:** macOS only
- **Permissions:** Automation access required
- **Prerequisite:** iCloud sync enabled for Reminders (optional)

## Tips & Gotchas

- Only works on macOS
- Automation permission must be granted first
- Reminders sync across all your Apple devices automatically
- For cross-platform task management, see [Todoist](./todoist.md)

## Related Skills

- [Todoist](./todoist.md) — Cross-platform task management alternative
- [CalDAV Calendar](./caldav-calendar.md) — Calendar integration
