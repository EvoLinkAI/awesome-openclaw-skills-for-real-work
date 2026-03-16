# Find Skills

> The most starred skill on ClawHub — searches for and installs skills from the open agent ecosystem directly from your agent.

**ClawHub:** https://clawhub.ai/JimLiuxinghai/find-skills · ⭐ 899 · installs: N/A  
**License:** MIT-0 · **API Key:** 🆓 Not required  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign)

---

## What It Does

Find Skills is the skill ecosystem's package manager. Describe what you need your agent to do ("find a skill for PR reviews" / "can you help with design?") and it searches the open agent skills registry, returns matching skills, and gives you the install command.

⭐899 — **the single most starred skill on ClawHub.** Install this first in every new setup.

## How to Install

```bash
clawhub install find-skills
```

## Key Capabilities

- Discover skills by keyword, domain, or use case
- Install skills from GitHub or the ClawHub registry
- Check for skill updates
- Update all installed skills in one command
- Browse skills at [https://skills.sh/](https://skills.sh/)

## Skills CLI (`npx skills`) Commands

| Command | What It Does |
|---------|--------------|
| `npx skills find [query]` | Search for skills interactively or by keyword |
| `npx skills add <package>` | Install a skill from GitHub or registry |
| `npx skills check` | Check for available skill updates |
| `npx skills update` | Update all installed skills to latest versions |

## Usage Examples

**Find a skill for a specific task:**
```
User: "I need a skill for reviewing pull requests"
Agent: > Runs `npx skills find pr review` and returns:
Install with `npx skills add <owner/repo@skill>`
vercel-labs/agent-skills@pr-review
octo-org/agent-tools@code-review
```

**Find a skill by domain:**
```
User: "find skills for React development"
Agent: > `npx skills find react best practices` → returns matching skills
```

**Update all skills:**
```
npx skills update
```

**Check for updates:**
```
npx skills check
```

## Requirements

- **Binaries:** `node`, `npm` (npx included with Node)
- **API Keys:** None
- **Platform:** All

## Tips & Gotchas

- Always read skill security notes before installing — not all skills are safe
- Use `npx skills check` regularly to keep skills updated
- Browse [skills.sh](https://skills.sh/) directly to discover new skills
- This skill is also known as "Skill Discovery" in some distributions

## Related Skills

- [Skill Vetter](https://clawhub.ai/spclaudehome/skill-vetter) — Audit any skill before installing
- [Auto-Updater Skill](#auto-updater-skill) — Automatically keep skills updated
- [Skill Creator](https://clawhub.ai/chindden/skill-creator) ⚠️ — Create new skills from within your agent
