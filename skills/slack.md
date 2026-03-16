# Slack

> React, send, edit, delete messages, manage pins, and fetch member info in Slack — all from your agent via the built-in Slack tool.

**ClawHub:** https://clawhub.ai/steipete/slack · ⭐ 91 · 974 installs  
**License:** MIT-0 · **API Key:** 🔑 Required — Slack bot token (configured in Clawdbot)  
**Security:** ⚠️ Flagged (OpenClaw: Suspicious, high confidence — bot token not declared in metadata; verify token scope before installing)

---

## What It Does

Slack skill teaches your agent to use OpenClaw's built-in `slack` tool for full Slack integration — send messages to channels or DMs, edit/delete, react with emoji, pin important messages, list pinned items, fetch member info, and list custom emoji. 

⭐91 · 974 installs — one of the most-installed communication skills.

> ⚠️ **Security note:** The skill uses a Slack bot token already configured in your Clawdbot environment, but doesn't declare this dependency in its metadata. Before installing: verify the bot token's scope (use least-privilege scopes) and confirm which token will be used.

## How to Install

```bash
clawhub install slack
```

**Prerequisites:**
- Slack bot configured in your Clawdbot environment
- Bot token with appropriate scopes: `chat:write`, `reactions:write`, `pins:write`, `users:read`

## Key Capabilities

- React to messages with any emoji
- List reactions on a message
- Send messages to channels or DMs
- Edit and delete messages
- Read recent channel messages
- Pin and unpin messages
- List all pinned items in a channel
- Fetch member info by user ID
- List custom workspace emoji

## Usage Examples

**React with ✅ to mark a task done:**
```json
{
  "action": "react",
  "channelId": "C123",
  "messageId": "1712023032.1234",
  "emoji": "✅"
}
```

**Send a message:**
```json
{
  "action": "sendMessage",
  "to": "channel:C123",
  "content": "Deploy complete — all systems green"
}
```

**Read recent messages:**
```json
{
  "action": "readMessages",
  "channelId": "C123",
  "limit": 20
}
```

**Pin a key decision:**
```json
{
  "action": "pinMessage",
  "channelId": "C123",
  "messageId": "1712023032.1234"
}
```

**Get member info:**
```json
{
  "action": "memberInfo",
  "userId": "U123"
}
```

## Action Reference

| Action | What It Does |
|--------|-------------|
| `react` | Add emoji reaction to a message |
| `reactions` | List reactions on a message |
| `sendMessage` | Send to channel or DM |
| `editMessage` | Update message text |
| `deleteMessage` | Delete a message |
| `readMessages` | Read recent channel history |
| `pinMessage` | Pin a message |
| `unpinMessage` | Unpin a message |
| `listPins` | List all pinned items |
| `memberInfo` | Get user profile |
| `emojiList` | List custom workspace emoji |

## Requirements

- **Binaries:** None (uses built-in `slack` tool)
- **API Keys:** Slack bot token configured in Clawdbot environment
- **Platform:** All

## Tips & Gotchas

- Message IDs in Slack are timestamps (e.g., `1712023032.1234`) — get them from `readMessages`
- Channel IDs start with `C`, user IDs start with `U` — use `memberInfo` to look up users
- The `to` field for `sendMessage` uses format `channel:C123` or `user:U123`
- Use `react` with `✅` to build lightweight task-tracking workflows
- Pin decisions and weekly status updates for easy retrieval later

## Related Skills

- [Discord](https://clawhub.ai/steipete/discord) — Same pattern for Discord
- [Gmail](./gmail.md) — Email integration for non-Slack communication
- [n8n Workflow Automation](./n8n-workflow-automation.md) — Automate Slack-triggered workflows
