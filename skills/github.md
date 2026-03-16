# GitHub

> Control GitHub from chat — issues, PRs, CI runs, and API queries via the `gh` CLI.

**ClawHub:** https://clawhub.ai/steipete/github · ⭐ 373 · 2,800 installs  
**License:** MIT-0 · **API Key:** 🔑 Requires `gh` CLI authenticated with GitHub  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign, high confidence)

---

## What It Does

This skill teaches your agent to use the official `gh` CLI to interact with GitHub programmatically. Check CI status on any PR, view failed workflow logs, list open issues, query the API with JQ filters — all without opening a browser. Particularly powerful for monitoring repos and triaging issues from your agent.

One of the highest-installed skills in the ecosystem (2,800+ installs, ⭐373).

## How to Install

```bash
clawhub install github
```

**Prerequisites:** Install and authenticate the `gh` CLI first:
```bash
brew install gh      # macOS
gh auth login        # Authenticate
```

## Key Capabilities

- Check CI status on any PR
- List and view workflow runs — including failed step logs
- List, view, and manage issues
- Query GitHub API with `--json` + `--jq` for structured output
- Works on any repo without being in a git directory (use `--repo owner/repo`)

## Usage Examples

**Check CI on a PR:**
```bash
gh pr checks 55 --repo owner/repo
```

**View failed workflow logs:**
```bash
gh run list --repo owner/repo --limit 10
gh run view <run-id> --repo owner/repo --log-failed
```

**List issues as structured JSON:**
```bash
gh issue list --repo owner/repo --json number,title \
  --jq '.[] | "\(.number): \(.title)"'
```

**Fetch PR details via API:**
```bash
gh api repos/owner/repo/pulls/55 \
  --jq '.title, .state, .user.login'
```

**View a specific run with all steps:**
```bash
gh run view <run-id> --repo owner/repo
```

## Requirements

- **Binaries:** `gh` (GitHub CLI) — must be installed and authenticated
- **API Keys:** Uses `gh auth login` or `GITHUB_TOKEN` env var
- **Platform:** macOS · Linux · Windows

## Tips & Gotchas

- Always use `--repo owner/repo` when running outside a git directory
- `--json` + `--jq` is incredibly powerful — learn a few JQ patterns and you unlock everything
- Scope your `GITHUB_TOKEN` to the minimum permissions needed — don't use a full-access token
- `gh run view --log-failed` is the fastest way to diagnose CI failures without opening the browser
- `gh pr checks` gives a quick pass/fail summary; `gh run view` gives the details

## Related Skills

- [Git Essentials](./git-essentials.md) — Local Git operations that complement `gh` for remote
- [Security Auditor](./security-auditor.md) — Audit code before merging PRs
- [n8n Workflow Automation](./n8n-workflow-automation.md) — Automate GitHub-triggered workflows
