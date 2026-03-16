# Discord

> Manage Discord servers, send messages, moderate channels, and interact with Discord communities directly from your agent.

**ClawHub:** https://clawhub.ai/steipete/discord · ⭐ 48 · 884 installs  
**License:** MIT-0 · **API Key:** 🔑 Required — Discord bot token  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign)

---

## What It Does

Discord skill lets your agent control a Discord bot — send messages to channels/DMs, moderate content, manage roles, list members, and interact with communities. Perfect for community managers, server owners, and anyone who wants to automate Discord workflows.

## How to Install

```bash
clawhub install discord
```

**Setup:**
1. Create a Discord bot at [discord.com/developers](https://discord.com/developers/applications)
2. Add the bot to your server with appropriate permissions
3. Set env var: `export DISCORD_BOT_TOKEN="your-bot-token"`

## Key Capabilities

- Send messages to channels and DMs
- Edit and delete messages
- Manage roles: add/remove roles from members
- Moderate content: kick/ban members, delete spam
- List members, channels, and roles
- Create channels and categories
- React to messages with emojis

## Usage Examples

**Send a message to a channel:**
```
"Send a message to #announcements channel: 'Server maintenance tonight at 10pm UTC — expect 30 minutes of downtime'"
```

**Moderate a user:**
```
"Kick user @spammer123 from the server for posting spam"
```

**Manage roles:**
```
"Give the 'Contributor' role to user @new-member"
```

**List server members:**
```
"Show me all members in the server with the 'Admin' role"
```

## Requirements

- **Binaries:** `python3`, `discord.py`
- **API Keys:** Discord bot token
- **Platform:** All

## Tips & Gotchas

- Use least privilege: only give the bot the permissions it actually needs
- Never share your bot token publicly
- Enable "Message Content Intent" in the Discord Developer Portal if your bot needs to read message content
- Pair with [Proactive Agent](./proactive-agent.md) for automated moderation alerts and community announcements

## Related Skills

- [Slack](./slack.md) — Slack integration alternative
- [n8n Workflow Automation](./n8n-workflow-automation.md) — Automate Discord workflows
