# Apple Notes

> Read and write Apple Notes directly from your agent — syncs across all your Apple devices.

**ClawHub:** https://clawhub.ai/steipete/apple-notes · ⭐ 40 · 947 installs  
**License:** MIT-0 · **API Key:** 🆓 Not required (uses macOS native AppleScript)  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign)

---

## What It Does

Apple Notes skill lets your agent interact with your Apple Notes library on macOS. Create new notes, read existing notes, append content, and search your notes. Perfect for Apple ecosystem users who keep their notes in Apple Notes.

## How to Install

```bash
clawhub install apple-notes
```

**Setup:** Grant automation permission to your terminal/agent environment in macOS System Settings > Privacy & Security > Automation.

## Key Capabilities

- Create new notes in any folder
- Read content from existing notes
- Append content to notes
- Search notes by title or content
- List folders and notes
- Syncs automatically across all Apple devices via iCloud

## Usage Examples

**Create a new note:**
```
"Create a new note in the 'Work' folder titled 'Q2 Goals' with the content I just gave you"
```

**Append to an existing note:**
```
"Append these meeting notes to the 'Team Meeting Notes' note"
```

**Search notes:**
```
"Find all notes in my library that mention 'OpenClaw'"
```

## Requirements

- **Binaries:** macOS built-in AppleScript
- **API Keys:** None
- **Platform:** macOS only
- **Permissions:** Automation access required
- **Prerequisite:** iCloud sync enabled for Apple Notes (optional)

## Tips & Gotchas

- Only works on macOS
- Automation permission must be granted first
- Notes are synced across all your Apple devices automatically
- For cross-platform note-taking, see [Obsidian](./obsidian.md) or [Notion](./notion.md)

## Related Skills

- [Obsidian](./obsidian.md) — Cross-platform alternative note-taking
- [Notion](./notion.md) — Cloud-based note-taking and knowledge base
