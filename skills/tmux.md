# Tmux

> Remote-control tmux sessions from your agent — send keystrokes, capture output, and orchestrate multiple terminal processes in parallel.

**ClawHub:** https://clawhub.ai/steipete/tmux · ⭐ 31 · 987 installs  
**License:** MIT-0 · **API Key:** 🆓 Not required  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign, high confidence)

---

## What It Does

Tmux lets your agent control terminal sessions that persist beyond the agent's own process. It can start interactive CLI tools, send commands, wait for output patterns, and capture results — all without a direct TTY. The killer use case: running multiple coding agents (Codex, Claude Code) in parallel in separate tmux sessions and monitoring them all from one place.

Use this when you need interactive CLIs (Python REPL, long builds, interactive tools) that can't run in a standard background process.

## How to Install

```bash
clawhub install tmux
```

## Key Capabilities

- Create isolated tmux sessions with custom socket paths
- Send keystrokes and commands to any pane (`send-keys`)
- Capture pane output — read terminal history programmatically
- Wait for specific text patterns before proceeding (`wait-for-text.sh`)
- Find and list all existing sessions across sockets
- Orchestrate multiple parallel coding agent sessions
- Works on macOS and Linux (WSL on Windows)

## Usage Examples

**Start a Python REPL in a tmux session:**
```bash
SOCKET_DIR="${CLAWDBOT_TMUX_SOCKET_DIR:-${TMPDIR:-/tmp}/clawdbot-tmux-sockets}"
mkdir -p "$SOCKET_DIR"
SOCKET="$SOCKET_DIR/clawdbot.sock"
SESSION=clawdbot-python

tmux -S "$SOCKET" new -d -s "$SESSION" -n shell
tmux -S "$SOCKET" send-keys -t "$SESSION":0.0 -- 'PYTHON_BASIC_REPL=1 python3 -q' Enter
tmux -S "$SOCKET" capture-pane -p -J -t "$SESSION":0.0 -S -200
```

**Run 5 coding agents in parallel:**
```bash
SOCKET="${TMPDIR:-/tmp}/codex-army.sock"

for i in 1 2 3 4 5; do
  tmux -S "$SOCKET" new-session -d -s "agent-$i"
done

tmux -S "$SOCKET" send-keys -t agent-1 "cd /tmp/project1 && codex --yolo 'Fix bug X'" Enter
tmux -S "$SOCKET" send-keys -t agent-2 "cd /tmp/project2 && codex --yolo 'Fix bug Y'" Enter
```

**Poll for completion:**
```bash
for sess in agent-1 agent-2; do
  if tmux -S "$SOCKET" capture-pane -p -t "$sess" -S -3 | grep -q "❯"; then
    echo "$sess: DONE"
  else
    echo "$sess: Running..."
  fi
done
```

**Wait for a specific prompt before sending next command:**
```bash
# Uses the bundled wait-for-text.sh helper
wait-for-text.sh -t session:0.0 -p 'pattern' -T 20
```

**Cleanup:**
```bash
tmux -S "$SOCKET" kill-session -t "$SESSION"   # Kill one session
tmux -S "$SOCKET" kill-server                  # Kill everything on socket
```

## Requirements

- **Binaries:** `tmux`
- **API Keys:** None
- **Platform:** macOS · Linux (WSL supported on Windows)
- **Env var:** `CLAWDBOT_TMUX_SOCKET_DIR` (optional, defaults to `${TMPDIR:-/tmp}/clawdbot-tmux-sockets`)

## Tips & Gotchas

- Use `PYTHON_BASIC_REPL=1` when launching Python — the default REPL breaks `send-keys` flows
- Always use isolated sockets (`-S path`) — don't attach to the system's default tmux server
- Use `--` before commands in `send-keys` to prevent flag misinterpretation
- Detect shell completion by looking for prompt characters (`❯`, `$`, `%`)
- Use separate git worktrees for parallel coding agents — no branch conflicts
- The bundled `wait-for-text.sh` script is essential for reliable sequencing

## Related Skills

- [Git Essentials](./git-essentials.md) — Run git operations in persistent sessions
- [Docker Essentials](./docker-essentials.md) — Monitor long-running container processes
- [GitHub](./github.md) — Monitor CI runs while agents work in parallel sessions
