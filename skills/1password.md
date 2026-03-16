# 1Password

> Access your 1Password vault directly from your agent — get secrets, passwords, API keys, and TOTP codes securely.

**ClawHub:** https://clawhub.ai/steipete/1password · ⭐ 34 · 872 installs  
**License:** MIT-0 · **API Key:** 🔑 Required — 1Password CLI authenticated  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign)

---

## What It Does

1Password skill lets your agent securely access your 1Password vault via the official 1Password CLI. Retrieve passwords, API keys, TOTP codes, and other secrets without hardcoding them into prompts or config files. The most secure way to give your agent access to credentials.

## How to Install

```bash
clawhub install 1password
```

**Setup:**
1. Install [1Password CLI](https://developer.1password.com/docs/cli/)
2. Authenticate: `op signin`
3. Ensure biometric unlock is enabled for passwordless access

## Key Capabilities

- Retrieve passwords, API keys, and secrets from your vault
- Generate TOTP codes for 2FA-protected accounts
- List vault items and search by name/title
- Create new vault entries
- Update existing secrets
- No hardcoding of credentials in prompts or files

## Usage Examples

**Get an API key:**
```
"Get the OPENAI_API_KEY from my 1Password vault"
```

**Generate a TOTP code:**
```
"Get the 2FA code for my GitHub account"
```

**Search for an item:**
```
"Find all items in my vault related to AWS"
```

**Create a new secret:**
```
"Create a new 1Password entry: 'MATON_API_KEY' with value 'my-secret-key' in the 'API Keys' vault"
```

## Requirements

- **Binaries:** 1Password CLI (`op`)
- **API Keys:** None (uses 1Password account authentication)
- **Platform:** macOS · Linux · Windows

## Tips & Gotchas

- Enable biometric unlock in 1Password settings for frictionless access
- Use least privilege: only give the agent access to vault items it actually needs
- Never output secrets in plain text unless explicitly requested
- Secrets are never stored in agent memory or logs
- Pair with [API Gateway](./api-gateway.md) to automatically inject secrets into API requests

## Related Skills

- [Security Auditor](./security-auditor.md) — Audit secret usage and ensure no leakage
- [OpenClaw Backup](./openclaw-backup.md) — Backup your 1Password config securely
