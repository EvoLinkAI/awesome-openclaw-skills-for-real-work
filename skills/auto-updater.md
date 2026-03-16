# Auto-Updater Skill

> Automatically keep all your installed skills up to date — no manual `clawhub sync` required.

**ClawHub:** https://clawhub.ai/maximeprades/auto-updater · ⭐ 280 · 747 installs  
**License:** MIT-0 · **API Key:** 🆓 Not required  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign)

---

## What It Does

Auto-Updater runs in the background and syncs all your installed skills to the latest version on a regular schedule. No more running `clawhub sync` manually or being stuck on old versions.

⭐280 · 747 installs. Works hand-in-hand with [Find Skills](./find-skills.md) to keep your skill set current.

## How to Install

```bash
clawhub install auto-updater
```

## Key Capabilities

- Automatic background sync of all installed skills
- Configurable sync schedule (default: daily)
- Update notifications sent to your agent chat
- Rollback to previous version if a skill breaks
- Skip list for skills you want to keep at a specific version
- Dry run mode to preview updates before applying

## Usage Examples

**Check current update schedule:**
```
"Show auto-updater schedule"
```

**Force an immediate sync:**
```
"Run skill update now"
```

**Add a skill to skip list:**
```
"Don't auto-update the memory-setup skill"
```

**View update history:**
```
"Show last 10 skill updates"
```

**Rollback a broken skill:**
```
"Rollback gmail skill to previous version"
```

## Default Schedule
| Frequency | What Runs |
|-----------|-----------|
| Daily (3am UTC) | Full sync of all skills, notify if any updated |
| Weekly (Sunday 2am UTC) | Full audit of all skills, check for security flags |

## Requirements

- **Binaries:** `clawhub` CLI
- **API Keys:** None
- **Platform:** macOS · Linux · Windows (with ClawHub CLI installed)

## Tips & Gotchas

- Always test updates in a staging environment first if you rely on critical skills
- The skip list is useful for custom modified skills you don't want overwritten
- Updates are idempotent — no changes if already on latest version
- Enable rollback backups in config to recover quickly from bad updates
- Configure notifications to alert you when skills are updated

## Related Skills

- [Find Skills](./find-skills.md) — Discover and install new skills
- [Skill Vetter](https://clawhub.ai/spclaudehome/skill-vetter) — Audit new versions before updating
- [OpenClaw Backup](./openclaw-backup.md) — Backup config before running bulk updates
