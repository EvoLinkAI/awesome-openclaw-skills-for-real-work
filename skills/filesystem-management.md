# Filesystem Management

> Advanced file listing, search, batch copy, and directory analysis — filter by type, size, date, and pattern from your agent.

**ClawHub:** https://clawhub.ai/gtrusler/clawdbot-filesystem · ⭐ 60 · 197 installs  
**License:** MIT-0 · **API Key:** 🆓 Not required  
**Security:** ⚠️ Flagged (OpenClaw: Suspicious — requires cloning external repo at runtime; review before installing)

---

## What It Does

Filesystem Management provides a structured CLI (`filesystem`) for file and directory operations that go beyond basic shell commands. It adds filtering by pattern, size, and date; recursive tree visualization; content search across files; and batch copy with dry-run preview. Designed for agents that need to navigate and manage complex project structures safely.

> ⚠️ **Security note:** The skill's SKILL.md instructs cloning a GitHub repo to obtain the `filesystem` binary — this is a network fetch of external code. Review the source repo (`https://github.com/gtrusler/clawdbot-filesystem`) before installing. The metadata mismatch between declared and actual requirements is worth noting.

## How to Install

```bash
clawhub install filesystem
```

Then follow the setup:
```bash
cd ~/.clawdbot/skills
git clone https://github.com/gtrusler/clawdbot-filesystem
chmod +x filesystem/filesystem
```

## Key Capabilities

- **Smart listing** — filter by type, pattern, size, date; sort by name/size/date; output as table, JSON, or list
- **Content search** — find files by name pattern or search inside file contents with context lines
- **Batch copy** — copy files matching a glob pattern with dry-run preview before execution
- **Tree view** — ASCII directory tree with depth control and file sizes
- **Directory analysis** — file counts, size distribution, type breakdown, largest files

## Usage Examples

**List all JS files recursively:**
```bash
filesystem list --path ./src --recursive --filter "*.js" --details
```

**Search for TODO/FIXME comments across source:**
```bash
filesystem search --pattern "TODO|FIXME" --path ./src --content --context 2
```

**Preview before copying logs to backup:**
```bash
filesystem copy --pattern "*.log" --to ./backup/logs/ --dry-run
filesystem copy --pattern "*.log" --to ./backup/logs/ --preserve  # execute
```

**Visualize project structure:**
```bash
filesystem tree --path ./ --depth 2 --size
```

**Find the 10 largest files in /var/log:**
```bash
filesystem analyze --path /var/log --sizes --largest 10
```

## Requirements

- **Binaries:** `node`, `git` (for cloning), `npm` (optional for global install)
- **API Keys:** None
- **Platform:** macOS · Linux

## Tips & Gotchas

- Always use `--dry-run` before any batch copy or delete operation
- `config.json` in the skill directory controls default exclude patterns (`node_modules`, `.git`, `.DS_Store`)
- The `--filter` flag accepts glob patterns; use quotes to prevent shell expansion
- Content search (`--content`) can be slow on large directories — narrow with `--path` first
- The skill includes path validation to prevent directory traversal — but always double-check paths before running destructive operations

## Related Skills

- [Git Essentials](./git-essentials.md) — Filesystem ops that respect `.gitignore`
- [Security Auditor](./security-auditor.md) — Validates filesystem operations in security-sensitive environments
- [OpenClaw Backup](./openclaw-backup.md) — Use alongside filesystem analysis for backup workflows
