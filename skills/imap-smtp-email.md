# IMAP/SMTP Email

> Universal email access via IMAP/SMTP — works with any email provider, no OAuth, no third-party services.

**ClawHub:** https://clawhub.ai/gzlicanyi/imap-smtp-email · ⭐ 56 · 228 installs  
**License:** MIT-0 · **API Key:** 🔑 Required — email account credentials  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign)

---

## What It Does

IMAP/SMTP Email gives your agent universal email access that works with any email provider: Gmail, Outlook, iCloud, Fastmail, self-hosted, and more. No OAuth flows, no third-party services, just standard IMAP for reading and SMTP for sending. Perfect for users who don't want to use the Maton API Gateway for email access.

## How to Install

```bash
clawhub install imap-smtp-email
```

**Setup:**
```bash
export IMAP_SERVER="imap.your-email.com"
export IMAP_PORT="993"
export IMAP_USERNAME="your-email@example.com"
export IMAP_PASSWORD="your-app-password"

export SMTP_SERVER="smtp.your-email.com"
export SMTP_PORT="587"
export SMTP_USERNAME="your-email@example.com"
export SMTP_PASSWORD="your-app-password"
```

## Key Capabilities

- Read emails from any folder (Inbox, Sent, Archive, etc.)
- Search emails by subject, sender, date, content
- Send emails with attachments
- Reply to and forward existing emails
- Mark emails as read/unread, archive, delete
- Works with **any** email provider that supports IMAP/SMTP
- No third-party services or OAuth required

## Usage Examples

**List recent emails:**
```
"Show me the last 10 unread emails in my Inbox"
```

**Search emails:**
```
"Find all emails from boss@company.com with 'urgent' in the subject from the past week"
```

**Send an email:**
```
"Send an email to team@company.com with subject 'Q2 Roadmap Draft' and body 'Attached is the Q2 roadmap draft for review.' Attach the roadmap.pdf file."
```

**Reply to an email:**
```
"Reply to the last email from john@example.com with: 'Thanks for the update, I'll review the document and get back to you by EOD.'"
```

**Mark emails as read:**
```
"Mark all unread emails from newsletter@example.com as read"
```

## Requirements

- **Binaries:** `python3`, `imaplib`, `smtplib` (Python standard library)
- **API Keys:** Email account credentials (use app-specific passwords for 2FA accounts)
- **Platform:** All

## Tips & Gotchas

- For Gmail, enable "Less secure app access" or use an app-specific password (recommended)
- Always use SSL/TLS connections (port 993 for IMAP, 587 for SMTP)
- Attachments are limited by your email provider's file size limits
- For Gmail users, see [Gmail](./gmail.md) for the managed OAuth alternative
- This skill never stores emails or credentials outside your local environment

## Related Skills

- [Gmail](./gmail.md) — Managed OAuth alternative for Gmail users
- [AgentMail](https://clawhub.ai/adboio/agentmail) — Higher-level email agent with scheduling and follow-ups
- [API Gateway](./api-gateway.md) — Alternative email access via Maton OAuth proxy
