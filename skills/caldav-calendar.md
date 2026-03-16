# CalDAV Calendar

> Full calendar integration via CalDAV — create events, list upcoming events, get reminders, sync with iCloud, Fastmail, Nextcloud, and more.

**ClawHub:** https://clawhub.ai/Asleep123/caldav-calendar · ⭐ 173 · 173 installs  
**License:** MIT-0 · **API Key:** 🔑 Required — CalDAV server credentials  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign)

---

## What It Does

CalDAV Calendar lets your agent access and manage your calendar via the CalDAV protocol, which works with almost every calendar service: iCloud, Fastmail, Nextcloud, Google Calendar (via CalDAV adapter), and self-hosted solutions. Create events, list upcoming appointments, get reminders, and sync across all your devices.

## How to Install

```bash
clawhub install caldav-calendar
```

**Setup:**
```bash
export CALDAV_URL="https://your-caldav-server.com"
export CALDAV_USERNAME="your-username"
export CALDAV_PASSWORD="your-app-password"
```

## Key Capabilities

- List upcoming events for any calendar
- Create new events with title, date, time, location, and description
- Update and delete existing events
- Get reminders for upcoming appointments
- Sync with all CalDAV-compatible services: iCloud, Fastmail, Nextcloud, Google Calendar
- Manage multiple calendars (personal, work, family, etc.)

## Usage Examples

**List today's events:**
```
"Show me all events on my calendar for today"
```

**Create a new event:**
```
"Create an event: 'Team Meeting' tomorrow at 2pm for 1 hour, location 'Zoom', add a description 'Discuss Q2 roadmap'"
```

**Check for conflicts:**
```
"Do I have any meetings next Wednesday at 3pm?"
```

**Get next week's schedule:**
```
"Show me my schedule for the entire next week"
```

**Delete an event:**
```
"Delete the 'Dentist Appointment' event on Friday"
```

## Requirements

- **Binaries:** `python3`, `caldav` Python package
- **API Keys:** CalDAV server credentials (username + password/app-specific password)
- **Platform:** All

## Tips & Gotchas

- For Google Calendar, use a CalDAV adapter or the official Google Calendar API instead
- Use app-specific passwords for services that support 2FA (iCloud, Fastmail, etc.)
- Always check for conflicting events before creating new ones
- Pair with [Proactive Agent](./proactive-agent.md) for meeting reminders and pre-meeting preparation
- Events are synced across all your devices connected to the same CalDAV account

## Related Skills

- [Todoist](./todoist.md) — Task management complement to calendar
- [Proactive Agent](./proactive-agent.md) — Event reminders and pre-meeting alerts
- [Home Assistant](./home-assistant.md) — Sync calendar events with smart home automations
