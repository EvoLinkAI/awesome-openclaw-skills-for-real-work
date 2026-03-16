# OpenClaw Backup

> Backup and restore your entire OpenClaw configuration — config, credentials, agents, workspace, and cron jobs — in one compressed archive.

**ClawHub:** https://clawhub.ai/alex3alex/openclaw-backup · ⭐ 43 · 143 installs  
**License:** MIT-0 · **API Key:** 🆓 Not required  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign)

---

## What It Does

OpenClaw Backup gives your agent a `backup.sh` script that archives your complete OpenClaw setup into a timestamped `.tar.gz` file. It captures everything that would be painful to rebuild: your config, API credentials, agent profiles, workspace memory, Telegram session, and cron schedules.

Keeps the last 7 backups automatically. Pairs perfectly with a daily cron job so you never lose your setup.

## How to Install

```bash
clawhub install openclaw-backup
```

## Key Capabilities

- One-command full backup of OpenClaw configuration
- Archives config, credentials, agents, workspace, Telegram session, and cron jobs
- Excludes cache and logs (regenerated automatically — no bloat)
- Keeps last 7 backups with automatic rotation
- Quick restore procedure (stop → extract → start)
- Schedule as a daily cron job with notification

## Usage Examples

**Manual backup:**
```bash
./scripts/backup.sh              # Default: ~/openclaw-backups/
./scripts/backup.sh /my/backup/  # Custom directory
# Output: openclaw-YYYY-MM-DD_HHMM.tar.gz
```

**What gets backed up:**
```
✅ openclaw.json      — main config
✅ credentials/       — API keys, tokens
✅ agents/            — agent configs, auth profiles
✅ workspace/         — memory, SOUL.md, user files
✅ telegram/          — session data
✅ cron/              — scheduled tasks

❌ completions/       — cache (auto-regenerated)
❌ *.log              — logs
```

**Schedule daily backup at 3am UTC:**
```json
{
  "name": "daily-backup",
  "schedule": {"kind": "cron", "expr": "0 3 * * *", "tz": "UTC"},
  "payload": {
    "kind": "agentTurn",
    "message": "Run ~/.openclaw/backup.sh and report result to user."
  },
  "sessionTarget": "isolated",
  "delivery": {"mode": "announce"}
}
```

**Quick restore:**
```bash
openclaw gateway stop
mv ~/.openclaw ~/.openclaw-old
tar -xzf ~/openclaw-backups/openclaw-YYYY-MM-DD_HHMM.tar.gz -C ~
openclaw gateway start
```

## Requirements

- **Binaries:** `tar`, `bash`
- **API Keys:** None
- **Platform:** macOS · Linux

## Tips & Gotchas

- Store backups off-machine (external drive, cloud storage) — a local backup doesn't help if the machine fails
- Your `credentials/` directory contains sensitive API keys — encrypt the backup archive or use a secure backup destination
- Run a test restore in a temp location before you actually need it
- The 7-backup rotation means ~1 week of daily backups — extend the script if you need more history
- After a restore, verify Telegram session is still valid — it may need re-authentication

## Related Skills

- [Model Usage](./model-usage.md) — Know what's worth preserving before backing up
- [Filesystem Management](./filesystem-management.md) — Inspect backup archives and find old configs
- [n8n Workflow Automation](./n8n-workflow-automation.md) — Build more sophisticated backup pipelines
