# API Gateway

> One Maton API key to access 100+ third-party APIs (Google, Microsoft, GitHub, Notion, Slack, HubSpot, Airtable, and more) with fully managed OAuth — no per-service token juggling.

**ClawHub:** https://clawhub.ai/byungkyu/api-gateway · ⭐ 223 · 279 installs  
**License:** MIT-0 · **API Key:** 🔑 Required — `MATON_API_KEY` from [maton.ai](https://maton.ai/)  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign)

---

## What It Does

API Gateway proxies your requests to 100+ third-party APIs through [Maton](https://maton.ai/)'s managed OAuth infrastructure. Instead of setting up OAuth flows, managing refresh tokens, and storing credentials for each service separately, you get one API key that handles authentication for all connected services automatically.

Call the native Slack API, Gmail API, or HubSpot API directly — Maton injects the correct OAuth token for you. This is the skill for agents that need to touch multiple external services without becoming a credential management nightmare.

## How to Install

```bash
clawhub install api-gateway
```

**Setup:**
1. Create an account at [maton.ai](https://maton.ai/)
2. Get your API key from [maton.ai/settings](https://maton.ai/settings)
3. Set the environment variable: `export MATON_API_KEY="your-key"`
4. Connect each service (Slack, Gmail, etc.) via the Maton dashboard

## Key Capabilities

- Proxy requests to any connected service's native API
- Automatic OAuth token injection — no manual token handling
- List and manage active service connections
- Create new connections programmatically
- Supports 100+ services: Google Workspace, Microsoft 365, GitHub, Notion, Slack, HubSpot, Salesforce, Airtable, and more

## Usage Examples

**Send a Slack message via native API:**
```python
import urllib.request, os, json

data = json.dumps({'channel': 'C0123456', 'text': 'Hello from gateway!'}).encode()
req = urllib.request.Request(
    'https://gateway.maton.ai/slack/api/chat.postMessage',
    data=data, method='POST'
)
req.add_header('Authorization', f'Bearer {os.environ["MATON_API_KEY"]}')
req.add_header('Content-Type', 'application/json')
print(json.dumps(json.load(urllib.request.urlopen(req)), indent=2))
```

**List all active connections:**
```python
import urllib.request, os, json

req = urllib.request.Request('https://ctrl.maton.ai/connections?status=ACTIVE')
req.add_header('Authorization', f'Bearer {os.environ["MATON_API_KEY"]}')
print(json.dumps(json.load(urllib.request.urlopen(req)), indent=2))
```

**URL pattern for any service:**
```
https://gateway.maton.ai/{app}/{native-api-path}

# Gmail example:
https://gateway.maton.ai/google-mail/gmail/v1/users/me/messages

# GitHub example:
https://gateway.maton.ai/github/repos/owner/repo/issues
```

## Requirements

- **Binaries:** None (pure HTTP calls)
- **API Keys:** `MATON_API_KEY` — from [maton.ai/settings](https://maton.ai/settings)
- **Platform:** All

## Tips & Gotchas

- The URL path MUST start with the app name (e.g., `/google-mail/...`, `/slack/...`) — this tells the gateway which OAuth connection to use
- Each service must be connected in the Maton dashboard first before you can proxy to it
- Use `https://ctrl.maton.ai/connections` to check connection status before debugging API failures
- The gateway injects OAuth tokens transparently — you never see or store the per-service tokens yourself
- Filter connections by app: `?app=slack&status=ACTIVE`

## Related Skills

- [Gmail](./gmail.md) — Higher-level Gmail interface (vs raw API calls here)
- [Slack](./slack.md) — Higher-level Slack interface
- [n8n Workflow Automation](./n8n-workflow-automation.md) — Automate multi-service workflows
- [GitHub](./github.md) — `gh` CLI alternative for GitHub operations
