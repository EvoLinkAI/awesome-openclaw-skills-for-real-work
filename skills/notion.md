# Notion

> Full Notion API access — create, read, update pages and databases, append blocks, search workspace — directly from your agent.

**ClawHub:** https://clawhub.ai/steipete/notion · ⭐ 188 · installs: N/A  
**License:** MIT-0 · **API Key:** 🔑 Required — Notion Integration token from [notion.so/my-integrations](https://notion.so/my-integrations)  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign)

---

## What It Does

Notion skill gives your agent direct access to the Notion API — create new pages, read existing ones, update content, query databases, and search across your workspace. Use it as your agent's external knowledge base, project tracker, or writing destination.

The skill uses Notion's API version `2025-09-03` (latest). Note: databases are called "data sources" in this version.

## How to Install

```bash
clawhub install notion
```

**Setup:**
```bash
# 1. Create integration at notion.so/my-integrations
# 2. Store your key
mkdir -p ~/.config/notion
echo "ntn_your_key_here" > ~/.config/notion/api_key

# 3. Share pages with your integration:
#    Click "..." on any page → "Connect to" → your integration name
```

## Key Capabilities

- Search across all connected pages and databases
- Read page content (blocks) and metadata
- Create new pages in databases
- Update existing pages and blocks
- Append content blocks to any page
- Query databases with filters and sorts
- Manage page properties

## Usage Examples

**Search your workspace:**
```bash
NOTION_KEY=$(cat ~/.config/notion/api_key)

curl -X POST "https://api.notion.com/v1/search" \
  -H "Authorization: Bearer $NOTION_KEY" \
  -H "Notion-Version: 2025-09-03" \
  -H "Content-Type: application/json" \
  -d '{"query": "project roadmap"}'
```

**Get a page:**
```bash
curl "https://api.notion.com/v1/pages/{page_id}" \
  -H "Authorization: Bearer $NOTION_KEY" \
  -H "Notion-Version: 2025-09-03"
```

**Read page blocks (content):**
```bash
curl "https://api.notion.com/v1/blocks/{page_id}/children" \
  -H "Authorization: Bearer $NOTION_KEY" \
  -H "Notion-Version: 2025-09-03"
```

**Create a new page in a database:**
```bash
curl -X POST "https://api.notion.com/v1/pages" \
  -H "Authorization: Bearer $NOTION_KEY" \
  -H "Notion-Version: 2025-09-03" \
  -H "Content-Type: application/json" \
  -d '{
    "parent": {"database_id": "your-database-id"},
    "properties": {
      "Name": {"title": [{"text": {"content": "New Entry"}}]}
    }
  }'
```

**Append text to a page:**
```bash
curl -X PATCH "https://api.notion.com/v1/blocks/{page_id}/children" \
  -H "Authorization: Bearer $NOTION_KEY" \
  -H "Notion-Version: 2025-09-03" \
  -H "Content-Type: application/json" \
  -d '{
    "children": [{
      "paragraph": {
        "rich_text": [{"text": {"content": "New content added by agent"}}]
      }
    }]
  }'
```

## Requirements

- **Binaries:** `curl` (or Python/any HTTP client)
- **API Keys:** Notion integration token (`ntn_...` or `secret_...`) — free, from [notion.so/my-integrations](https://notion.so/my-integrations)
- **Platform:** All

## Tips & Gotchas

- Every page must be explicitly shared with your integration — it won't see pages you haven't connected
- The `Notion-Version: 2025-09-03` header is required on every request — don't omit it
- Page IDs can be found in the URL: `notion.so/Page-Title-{page_id}`
- `search` returns both pages and databases — filter with `"filter": {"property": "object", "value": "page"}`
- Databases in API v2025 are called "data sources" — the skill notes this explicitly
- Integration token has read/write access to everything you share — don't over-share sensitive pages

## Related Skills

- [Obsidian](https://clawhub.ai/steipete/obsidian) — Local-first alternative to Notion
- [Memory Setup](./memory-setup.md) — Use Notion as external memory layer
- [Summarize](./summarize.md) — Summarize content before writing to Notion
- [API Gateway](./api-gateway.md) — Alternative Notion access via Maton OAuth proxy
