# Todoist

> Full Todoist integration — create, update, complete tasks, manage projects, and get reminders directly from your agent.

**ClawHub:** https://clawhub.ai/mjrussell/todoist · ⭐ 43 · 154 installs  
**License:** MIT-0 · **API Key:** 🔑 Required — `TODOIST_API_KEY` from Todoist Developer Settings  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign)

---

## What It Does

Todoist skill gives your agent complete access to your Todoist account. Create tasks, set due dates/priorities, complete tasks, manage projects, and query your task list. The perfect productivity companion for your agent.

## How to Install

```bash
clawhub install todoist
```

**Setup:**
1. Get your API key from [Todoist Developer Settings](https://developer.todoist.com/rest/v2/#overview)
2. Set env var: `export TODOIST_API_KEY="your-key"`

## Key Capabilities

- Create new tasks with due dates, priorities, projects, and labels
- List tasks from any project or filter
- Complete and re-open tasks
- Update task details: due date, priority, content, project
- Manage projects: create, list, archive
- Get productivity stats and completed tasks history
- Set up reminders for tasks

## Usage Examples

**Create a new task:**
```
"Create a task: 'Finish awesome-openclaw-skills README'
Due tomorrow, priority 1, project 'Open Source'"
```

**List today's tasks:**
```
"Show me all tasks due today"
```

**Complete a task:**
```
"Mark task 'Write first 20 skill docs' as complete"
```

**Project overview:**
```
"Show me all tasks in the 'Open Source' project"
```

**Productivity stats:**
```
"How many tasks did I complete last week?"
```

## Requirements

- **Binaries:** None
- **API Keys:** `TODOIST_API_KEY` — free from [developer.todoist.com](https://developer.todoist.com/)
- **Platform:** All

## Tips & Gotchas

- Use natural language for due dates: "tomorrow at 3pm", "next Friday", "every Monday"
- Priority levels: 1 (highest) to 4 (lowest)
- Filter tasks using Todoist's query syntax: "due:today & priority:1"
- Webhooks are available for real-time updates
- For reminders, pair with [Proactive Agent](./proactive-agent.md)

## Related Skills

- [Apple Reminders](https://clawhub.ai/steipete/apple-reminders) — macOS native alternative
- [Calendar Integration](https://clawhub.ai/Asleep123/caldav-calendar) — Sync tasks with your calendar
- [Proactive Agent](./proactive-agent.md) — Proactive task reminders and follow-ups
