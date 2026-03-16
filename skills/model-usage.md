# Model Usage

> Track per-model AI cost from CodexBar's local cost logs — see what's expensive, compare models, and optimize your spending.

**ClawHub:** https://clawhub.ai/steipete/model-usage · ⭐ 88 · installs: N/A  
**License:** MIT-0 · **API Key:** 🆓 Not required  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign)

---

## What It Does

Model Usage reads CodexBar's local cost logs and summarizes what each AI model is costing you — current session, daily breakdown, or all-time by model. Useful when you're running multiple models and want to know where the spend is going without manually parsing JSON files.

Works with both Codex and Claude provider logs. Requires CodexBar to be installed and logging costs locally.

## How to Install

```bash
clawhub install model-usage
```

**Prerequisite:** [CodexBar](https://codexbar.app/) must be installed and actively logging cost data.

## Key Capabilities

- Get current model cost (most recent daily entry, highest-cost model)
- Summarize all models across all recorded days
- Supports both Codex and Claude providers
- JSON output for programmatic use
- Works from CLI, file input, or stdin
- Bundled Python script — no extra dependencies beyond Python

## Usage Examples

**Current model cost (most expensive today):**
```bash
python {baseDir}/scripts/model_usage.py --provider codex --mode current
```

**All models, all time:**
```bash
python {baseDir}/scripts/model_usage.py --provider codex --mode all
python {baseDir}/scripts/model_usage.py --provider claude --mode all
```

**Pretty JSON output:**
```bash
python {baseDir}/scripts/model_usage.py --provider claude --mode all --format json --pretty
```

**From a saved cost file:**
```bash
codexbar cost --provider codex --format json > /tmp/cost.json
python {baseDir}/scripts/model_usage.py --input /tmp/cost.json --mode all
```

**Pipe from codexbar:**
```bash
cat /tmp/cost.json | python {baseDir}/scripts/model_usage.py --input - --mode current
```

## Requirements

- **Binaries:** `python3`, CodexBar CLI (`codexbar`)
- **API Keys:** None
- **Platform:** macOS (Linux support documented as TODO in skill)

## Tips & Gotchas

- Cost data is pulled from CodexBar's local logs — if CodexBar isn't running or hasn't logged today, results will be empty or stale
- "Current model" picks the highest-cost model from the most recent daily row — override with `--model <name>` if you need a specific one
- Token counts are not split by model in CodexBar's output — only cost is broken down per model
- Linux CLI support is noted as TODO in the skill — macOS only for now
- Run `codexbar cost --format json --provider codex` first to verify you have data before invoking the skill

## Related Skills

- [OpenClaw Backup](./openclaw-backup.md) — Back up your OpenClaw config including cost logs
- [Auto-Updater Skill](https://clawhub.ai/maximeprades/auto-updater) — Keep skills updated as CodexBar evolves
- [Free Ride](https://clawhub.ai/Shaivpidadi/free-ride) — Route tasks to cheaper/free models to reduce costs
