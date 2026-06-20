# TweetClaw

> X/Twitter workflow plugin for OpenClaw: research public context, draft posts, prepare schedules, and keep account-affecting actions approval-gated.

**ClawHub:** https://clawhub.ai/plugins/@xquik/tweetclaw · ⭐ 75 GitHub stars  
**License:** MIT · **API Key:** 🔑 Required for live X/Twitter actions  
**Security:** ⚠️ Account-affecting actions must stay approval-gated

---

## What It Does

TweetClaw connects OpenClaw to X/Twitter workflows through the Xquik API. Use it when a content, research, or marketing agent needs public X/Twitter context before drafting or scheduling social posts.

It is most useful as a controlled workflow step: gather public evidence, prepare a draft, show the exact action to the operator, then run write-like actions only after approval.

## How to Install

```bash
openclaw plugins install clawhub:@xquik/tweetclaw
```

Canonical project links:

- GitHub: https://github.com/Xquik-dev/tweetclaw
- npm package: `@xquik/tweetclaw`

## Key Capabilities

- Search public X/Twitter posts and replies for source context
- Draft posts, replies, and thread outlines for review
- Prepare scheduled content workflows with a clear human approval step
- Export public follower and engagement context for analysis
- Coordinate with webhooks and monitoring workflows when configured
- Use OpenClaw plugin metadata instead of ad hoc scripts

## Usage Examples

**Research before drafting:**
```
"Find recent public X/Twitter posts about our launch topic, summarize the recurring objections, and draft 3 replies for review."
```

**Prepare a thread:**
```
"Draft a 5-post thread from these release notes. Show the final text and target account before any publishing action."
```

**Schedule with approval:**
```
"Prepare tomorrow's announcement post and ask for approval before scheduling it."
```

## Requirements

- **Runtime:** OpenClaw with plugin support
- **API Keys:** Xquik API credentials for live X/Twitter actions
- **Platform:** All platforms supported by OpenClaw

## Safety Notes

- Treat posting, replies, follows, direct messages, media uploads, and scheduling as approval-gated actions.
- Show the final text, target account, links, media, and timing before write-like actions.
- Do not place API keys, account tokens, browser cookies, or session material in prompts or public logs.
- Use TweetClaw for public-context workflows, not private messages, spam, harassment, impersonation, or automated engagement campaigns.

## Related Skills

- [Humanize AI text](./humanize-ai-text.md) — Polish social copy
- [Markdown Converter](./markdown-converter.md) — Prepare source material
- [News Summary](./news-summary.md) — Generate topic briefings before drafting
- [Proactive Agent](./proactive-agent.md) — Build approval-first recurring workflows
