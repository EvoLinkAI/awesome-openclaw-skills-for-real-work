🌐 **English** | [Español](README.es.md) | [한국어](README.ko.md) | [日本語](README.ja.md) | [Deutsch](README.de.md) | [Français](README.fr.md) | [Türkçe](README.tr.md) | [Русский](README.ru.md) | [Português](README.pt.md) | [简体中文](README.zh-CN.md) | [繁體中文](README.zh-TW.md)

# workspace-github-ops

This directory is an operations workspace, not a single product repository.

## Layout

- `repos/`: canonical git repositories
- `tasks/`: active task-specific working copies
- `artifacts/`: generated reports, traffic snapshots, CSV exports
- `tmp/`: disposable scratch files and temporary outputs
- `ops/`: operating docs, memory, and maintenance scripts
- `exports/`: non-source exports only; do not store duplicate repo copies here

## Notes

- Root-level dot directories such as `.openclaw/`, `.clawhub/`, and `.learnings/` are workspace metadata and were left in place.
- Root-level `AGENTS.md`, `SOUL.md`, `USER.md`, `MEMORY.md`, and `memory/` are intentional runtime/bootstrap files for this workspace and remain at the root.
- Historical root README translations were moved to `ops/docs/legacy-root-readmes/` because they described a subproject rather than this workspace.
- Two duplicate temporary repositories were removed: `.tmp/` and `.temp-repo/`.
- Duplicate exported repo copies were removed from `exports/`. The only unique nested repo that was preserved was moved to `repos/seedance-2-api/`.

## Expected Workflow

Use `repos/` for durable source-of-truth repositories. Use `tasks/active/` when a repo needs isolated in-progress work. Generated outputs should go to `artifacts/` or `tmp/`, not back into the root.
