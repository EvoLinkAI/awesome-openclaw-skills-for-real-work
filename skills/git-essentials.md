# Git Essentials

> The complete Git reference for your agent — commit, branch, merge, rebase, and recover, all from chat.

**ClawHub:** https://clawhub.ai/Arnarsson/git-essentials · ⭐ 23 · 145 installs  
**License:** MIT-0 · **API Key:** 🆓 Not required  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign, high confidence)

---

## What It Does

Git Essentials gives your agent a complete, battle-tested Git reference. It covers the full lifecycle: init, commit, branch, merge, rebase, stash, tag, remote sync, and recovery. Instead of Googling commands, your agent knows them — and can walk you through common workflows like feature branches, hotfixes, and fork syncing.

Useful when you want your agent to help with version control without you having to spell out every flag.

## How to Install

```bash
clawhub install git-essentials
```

## Key Capabilities

- Full staging and commit workflow (`add`, `commit`, `amend`)
- Branch management — create, switch, rename, delete
- Remote operations — fetch, pull, push, force-with-lease
- History search — `log`, `blame`, `bisect`, `grep`
- Undo and recovery — `reset`, `revert`, `restore`, `reflog`
- Stashing — save, list, apply, pop, drop
- Interactive rebase — squash, reorder, edit commits
- Tags — create, push, delete annotated and lightweight
- Cherry-pick and submodules
- Common workflow recipes

## Usage Examples

**Feature branch workflow:**
```bash
git checkout -b feature/new-feature
git add .
git commit -m "Add new feature"
git push -u origin feature/new-feature
# After PR merge:
git checkout main && git pull
git branch -d feature/new-feature
```

**Undo last commit (keep changes):**
```bash
git reset --soft HEAD~1
```

**Recover a deleted branch:**
```bash
git reflog
git checkout -b branch-name <commit-hash>
```

**Sync a fork:**
```bash
git remote add upstream https://github.com/original/repo.git
git fetch upstream
git checkout main
git merge upstream/main
git push origin main
```

**Search commit history:**
```bash
git log --grep="bug fix"          # Search messages
git log -S "function_name"        # Search code changes
git log --graph --oneline --all   # Visual branch graph
```

## Requirements

- **Binaries:** `git`
- **API Keys:** None
- **Platform:** macOS · Linux · Windows

## Tips & Gotchas

- Always use `--force-with-lease` instead of `--force` when pushing — it protects against overwriting others' work
- `git clean -fdx` is destructive — preview with `git clean -n` first
- `git reset --hard` discards all uncommitted changes permanently — no undo
- Add useful aliases to `~/.gitconfig`: `visual = log --graph --oneline --all`
- `git commit -am "msg"` only stages tracked files — new files still need `git add`

## Related Skills

- [GitHub](./github.md) — Use `gh` CLI for PRs, issues, and CI on top of Git
- [Tmux](./tmux.md) — Run long Git operations in persistent terminal sessions
- [Filesystem Management](./filesystem-management.md) — Navigate and manage files alongside Git ops
