# Security Auditor

> Senior application security engineer in a skill — OWASP Top 10 audits, vulnerability detection, and actionable secure coding fixes for your codebase.

**ClawHub:** https://clawhub.ai/jgarrison929/security-auditor · ⭐ 19 · 146 installs  
**License:** MIT-0 · **API Key:** 🆓 Not required  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign)

---

## What It Does

Security Auditor turns your agent into a senior AppSec engineer. Give it code, configs, or architecture descriptions and it conducts a structured security review against OWASP Top 10, designs secure auth flows, implements input validation, and provides concrete before/after code fixes — not just "you should validate input" hand-waving.

Adapted from buildwithclaude by Dave Poon (MIT license). Practical over theoretical.

## How to Install

```bash
clawhub install security-auditor
```

## Key Capabilities

- Full OWASP Top 10 (2021) audit framework
- Access control verification — ownership checks, RBAC, JWT validation
- Cryptographic review — password hashing, encryption at rest, TLS enforcement
- Injection prevention — SQL, XSS, command injection detection and fixes
- Input validation patterns — sanitization, schema validation, type checking
- Authentication flow design — secure session management, MFA, token rotation
- Security test generation — unit tests for auth boundaries and injection points
- Dependency scanning guidance and secrets detection

## Usage Examples

**Audit an API endpoint:**
```
"Audit this Express route for security issues:
app.delete('/api/posts/:id', async (req, res) => {
  await db.post.delete({ where: { id: req.params.id } })
  res.json({ success: true })
})"
```

Agent identifies missing auth check, provides the fix:
```typescript
// ✅ GOOD: Verify ownership
app.delete('/api/posts/:id', authenticate, async (req, res) => {
  const post = await db.post.findUnique({ where: { id: req.params.id } })
  if (!post) return res.status(404).json({ error: 'Not found' })
  if (post.authorId !== req.user.id && req.user.role !== 'admin') {
    return res.status(403).json({ error: 'Forbidden' })
  }
  await db.post.delete({ where: { id: req.params.id } })
  res.json({ success: true })
})
```

**Check password storage:**
```typescript
// ❌ BAD (flagged):
await db.user.create({ data: { password: req.body.password } })

// ✅ GOOD (suggested fix):
import bcrypt from 'bcryptjs'
const hashedPassword = await bcrypt.hash(req.body.password, 12)
await db.user.create({ data: { password: hashedPassword } })
```

**Request a full audit:**
```
"Review this authentication system for OWASP Top 10 issues.
Focus on A01 (Broken Access Control) and A07 (Auth failures)."
```

## Requirements

- **Binaries:** None
- **API Keys:** None
- **Platform:** All

## Tips & Gotchas

- Provide actual code, not descriptions — the agent gives much better output with real code to analyze
- Ask for specific OWASP categories when you know what you're targeting (e.g., "A03: Injection")
- Always review suggested fixes before applying — context matters and auto-fixes can introduce regressions
- For dependency scanning, also run actual tools (`npm audit`, `snyk`) — this skill complements but doesn't replace them
- Use this before every PR merge for sensitive code paths (auth, payments, data access)

## Related Skills

- [Git Essentials](./git-essentials.md) — Review code before committing
- [GitHub](./github.md) — Integrate security review into PR workflow
- [Docker Essentials](./docker-essentials.md) — Audit Dockerfile and container configurations
- [healthcheck](https://clawhub.ai/Stellarhold170NT/healthcheck) ⚠️ — System-level security hardening (review scan before installing)
