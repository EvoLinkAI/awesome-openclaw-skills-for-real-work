# Healthcheck

> System security hardening and health check tool. Scan for vulnerabilities, harden SSH/firewall settings, and check system configuration. ⚠️ Security flagged.

**ClawHub:** https://clawhub.ai/Stellarhold170NT/healthcheck · ⭐ 8 · 748 installs  
**License:** MIT-0 · **API Key:** 🆓 Not required  
**Security:** ⚠️ Flagged (OpenClaw: Suspicious patterns detected — review before running on production systems)

---

## What It Does

Healthcheck is a system security auditing and hardening tool. It scans your system for common vulnerabilities, checks SSH and firewall configurations, applies security hardening best practices, and generates a health report. Useful for securing new server installations.

> ⚠️ **Security warning:** This skill modifies system configuration files (SSH settings, firewall rules, sysctl parameters). Running it on production systems may break existing configurations or lock you out if something goes wrong. Review all scripts and changes before applying. Test in staging first.

## How to Install

```bash
# Review all code first before installing
clawhub install healthcheck
```

## Key Capabilities

- System vulnerability scanning
- SSH configuration hardening (disable root login, disable password auth, etc.)
- Firewall configuration and hardening
- System update and patch management checks
- Security best practices validation
- Generate security health reports
- Apply hardening configurations automatically

## Usage Examples

**Run a security scan:**
```
"Run a full security health check on this system and generate a report"
```

**Harden SSH configuration:**
```
"Harden the SSH configuration on this server to follow security best practices"
```

**Apply all hardening rules:**
```
"Apply all recommended security hardening configurations to this system"
```

## Requirements

- **Binaries:** Root/sudo access to modify system settings
- **API Keys:** None
- **Platform:** Linux only
- **Permissions:** Root privileges required for most operations

## Risks & Warnings

- ⚠️ Modifies critical system configuration files
- ⚠️ Can break existing network/SSH configurations if misconfigured
- ⚠️ May lock you out of the system if SSH settings are changed incorrectly
- ⚠️ Test in a staging environment before running on production
- ⚠️ Always back up configuration files before applying changes

## Alternatives

- [Security Auditor](./security-auditor.md) — Code and application security auditing (no system changes)
