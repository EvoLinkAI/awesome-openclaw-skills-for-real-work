# n8n Workflow Automation

> Design production-grade n8n workflows with retries, idempotency, error handling, and human-in-the-loop review queues — output as importable JSON.

**ClawHub:** https://clawhub.ai/KOwl64/n8n-workflow-automation · ⭐ 88 · 148 installs  
**License:** MIT-0 · **API Key:** 🆓 Not required  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign, high confidence)

---

## What It Does

This skill turns your agent into an n8n workflow architect. Describe what you want to automate — a Monday morning compliance email, a webhook that logs every run, a cron job that won't silently fail — and it outputs a production-ready `workflow.json` you can import directly into n8n, plus a `runbook.md` for operations.

The key differentiator: it enforces good automation hygiene by default. Every workflow it designs includes idempotency (no duplicate records on reruns), structured logging, retry with backoff, and a human review queue for failures.

## How to Install

```bash
clawhub install n8n-workflow-automation
```

## Key Capabilities

- Designs workflows with triggers: cron, webhook, or manual
- Enforces idempotency — dedup keys prevent duplicate records on retries
- Adds observability: `run_id` generation, start/end logging, status rows
- Per-node error branches with configurable retry and backoff
- Human-in-the-loop (HITL) review queue for failed items
- "No silent failure" gates — alerts if thresholds aren't met
- Outputs importable `workflow.json` + `runbook.md`
- Asks before proceeding when destination or credential strategy is unclear

## Usage Examples

**Describe your workflow in plain English:**
```
"Build an n8n workflow that runs every Monday at 8am London time,
fetches a compliance summary, emails it to the team, uploads to Drive,
and queues failures for human review."
```

**Agent outputs valid n8n JSON:**
```json
{
  "name": "Weekly Compliance Summary",
  "nodes": [
    { "name": "Trigger", "type": "n8n-nodes-base.cron", "parameters": {}, "position": [0,0] }
  ],
  "connections": {},
  "settings": {},
  "active": false
}
```

**Webhook workflow with logging:**
```
"Create a webhook workflow that receives JSON payloads,
validates required fields, writes a status row to a Google Sheet,
and sends a Slack alert on failure."
```

**Add resilience to an existing workflow:**
```
"Add error handling and retries to this workflow JSON [paste JSON],
plus a review queue that writes failures to Airtable."
```

## Requirements

- **Binaries:** None (instruction-only — generates JSON for you to import into n8n)
- **API Keys:** None required for the skill itself; your n8n instance uses its own credentials
- **Platform:** All (output is n8n-portable JSON)

## Tips & Gotchas

- Never paste real API keys or passwords into prompts — provide credential names only (e.g., `SLACK_BOT_TOKEN`), store actual keys in n8n's credential store
- Always test generated workflows in a staging n8n environment before production
- The skill will STOP AND ASK if destination systems, dedup keys, or credential strategy aren't clear — this is intentional
- Validate idempotency manually: run the workflow twice with the same input and verify no duplicates appear
- The bundled `runbook-template.md` is your operations manual — fill it in for every workflow you deploy

## Related Skills

- [GitHub](./github.md) — Trigger n8n workflows from GitHub events
- [Docker Essentials](./docker-essentials.md) — Run n8n self-hosted in Docker
- [Security Auditor](./security-auditor.md) — Audit automation scripts before deploying
- [API Gateway](./api-gateway.md) — Connect n8n to 100+ APIs with managed OAuth
