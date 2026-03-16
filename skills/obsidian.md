# Obsidian

> Read and write to your Obsidian vault directly from your agent — create notes, append content, search your knowledge base, link notes.

**ClawHub:** https://clawhub.ai/steipete/obsidian · ⭐ 205 · installs: N/A  
**License:** MIT-0 · **API Key:** 🆓 Not required (local files only)  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign)

---

## What It Does

Obsidian skill lets your agent work directly with your local Obsidian vault — create new notes, append content to existing notes, search your knowledge base, generate backlinks, and integrate your second brain with your agent workflow. Perfect for knowledge workers who use Obsidian as their main note-taking tool.

## How to Install

```bash
clawhub install obsidian
```

**Setup:**
```bash
# Point to your Obsidian vault directory
export OBSIDIAN_VAULT_PATH="/path/to/your/obsidian/vault"
```

## Key Capabilities

- Create new notes with Markdown content
- Append content to existing notes
- Search your entire vault for keywords/topics
- List all notes in a specific folder
- Generate backlinks and internal links
- Read content from any note in your vault
- No cloud sync required — works with local files only

## Usage Examples

**Create a new note:**
```
"Create a new note in the 'Research' folder titled 'Self-Improving Agents' with the content I just gave you"
```

**Append content to an existing note:**
```
"Append these key takeaways to the 'AI Agent Architecture' note"
```

**Search your vault:**
```
"Find all notes in my vault that mention 'memory architectures'"
```

**Read a note:**
```
"Read the 'Q2 Roadmap' note and summarize it for me"
```

**Generate daily note:**
```
"Create a daily note for today with a summary of the tasks I completed"
```

## Requirements

- **Binaries:** None (works with local files)
- **API Keys:** None
- **Platform:** All (works with local Obsidian vault directory)

## Tips & Gotchas

- Your vault remains fully local — no data is sent to any cloud services unless you explicitly sync it
- Use relative paths for folders within your vault
- Markdown links are preserved when creating/editing notes
- Pair with [Memory Manager](./memory-manager.md) to integrate your Obsidian vault with your agent's memory
- For Obsidian Sync users, changes made by the agent will sync to all your devices automatically

## Related Skills

- [Notion](./notion.md) — Cloud-based alternative to Obsidian
- [Memory Manager](./memory-manager.md) — Integrate Obsidian as an external memory layer
- [Summarize](./summarize.md) — Summarize long notes and research papers in your vault
