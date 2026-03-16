# Gmail

> Read, send, search, and manage Gmail via the native Gmail API — powered by Maton's managed OAuth. No browser, no OAuth dance.

**ClawHub:** https://clawhub.ai/byungkyu/gmail · ⭐ 60 · 219 installs  
**License:** MIT-0 · **API Key:** 🔑 Required — `MATON_API_KEY` from [maton.ai](https://maton.ai/)  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign)

---

## What It Does

Gmail skill gives your agent access to the full Gmail API through Maton's OAuth proxy — no OAuth flow to implement, no token refreshes to manage. Connect your Google account once on Maton's dashboard, then make native Gmail API calls with one API key.

Pairs naturally with [API Gateway](./api-gateway.md) — both use the same `MATON_API_KEY`.

## How to Install

```bash
clawhub install gmail
```

**Setup:**
1. Get `MATON_API_KEY` from [maton.ai/settings](https://maton.ai/settings)
2. Connect your Google account: `POST https://ctrl.maton.ai/connections` with `{"app": "google-mail"}`
3. Complete OAuth in the returned URL
4. `export MATON_API_KEY="your-key"`

## Key Capabilities

- List messages and threads with filters
- Read full email content
- Send emails (with attachments support via Gmail API)
- Create and manage drafts
- Manage labels
- Search with Gmail query syntax (`from:`, `subject:`, `has:attachment`, etc.)

## Usage Examples

**List recent messages:**
```python
import urllib.request, os, json

req = urllib.request.Request(
    'https://gateway.maton.ai/google-mail/gmail/v1/users/me/messages?maxResults=10'
)
req.add_header('Authorization', f'Bearer {os.environ["MATON_API_KEY"]}')
print(json.dumps(json.load(urllib.request.urlopen(req)), indent=2))
```

**Search for emails:**
```python
import urllib.parse
query = urllib.parse.quote('from:boss@company.com subject:urgent')
url = f'https://gateway.maton.ai/google-mail/gmail/v1/users/me/messages?q={query}'
# ... same request pattern
```

**Send an email:**
```python
import base64
from email.mime.text import MIMEText

msg = MIMEText("Email body here")
msg['to'] = 'recipient@example.com'
msg['subject'] = 'Subject line'

raw = base64.urlsafe_b64encode(msg.as_bytes()).decode()
data = json.dumps({"raw": raw}).encode()

req = urllib.request.Request(
    'https://gateway.maton.ai/google-mail/gmail/v1/users/me/messages/send',
    data=data, method='POST'
)
req.add_header('Authorization', f'Bearer {os.environ["MATON_API_KEY"]}')
req.add_header('Content-Type', 'application/json')
```

**Check active connection:**
```python
req = urllib.request.Request(
    'https://ctrl.maton.ai/connections?app=google-mail&status=ACTIVE'
)
req.add_header('Authorization', f'Bearer {os.environ["MATON_API_KEY"]}')
```

## Requirements

- **Binaries:** None (Python stdlib only)
- **API Keys:** `MATON_API_KEY` from [maton.ai](https://maton.ai/)
- **Platform:** All

## Tips & Gotchas

- The API gateway URL always starts with `/google-mail/` even though the native Gmail API path starts with `/gmail/v1/`
- `Notion-Version` header not needed here — this is Gmail not Notion; just Authorization header
- Message IDs from list calls are needed for read/delete — store them when listing
- Gmail search query syntax is powerful: `is:unread`, `has:attachment`, `after:2026/01/01`, `label:inbox`
- Sending requires base64url-encoded RFC 2822 message — use Python's `email.mime` module

## Related Skills

- [API Gateway](./api-gateway.md) — Same `MATON_API_KEY`, access 100+ other services
- [imap-smtp-email](https://clawhub.ai/gzlicanyi/imap-smtp-email) — Universal IMAP/SMTP alternative (no Maton required)
- [AgentMail](https://clawhub.ai/adboio/agentmail) — Higher-level email agent with scheduling
