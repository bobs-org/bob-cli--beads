# Bead: bob-cli-1w.1 — Project selector and structured check output for \`sase init\`

[Bead Pages](../README.md) / [bob-cli-1w](README.md) / bob-cli-1w.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.e](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.apollo.e.md) · **Assignee:** `bob-cli-1w.1` · **Size:** medium
**Created:** 2026-09-03 17:42:11 EDT · **Closed:** 2026-09-03 19:14:26 EDT
**Plan:** [202609/projects\_tab\_init.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/projects_tab_init.md)

## Description

cli: add the repeatable `-p/--project` selector beside `--all`, a `-j/--json` mode on `--check` with a schema version, per-planner `requires_tty` markers, and a status that distinguishes drift from blockers, lift the doctor plan serializer into `init_plan.py` without silent truncation, mirror the `--all`-with-subcommand dispatch guard for `-p`, and document both options.

## Notes

[2026-09-03T23:14:26Z · bob-cli-1w.1] sase init -p/--project (repeatable, exclusive with --all/-M, rejects subcommands) filters the enabled inventory into one batched chezmoi run; --json requires --check and emits one schema_version 1 document whose status distinguishes current, drift, and blocked despite identical exit codes; requires_tty is classified on owner-identity setup and provider sidecar creation; doctor uses the shared serializer with an explicit truncated marker and no silent action drop; docs/init.md, docs/cli.md, and docs/configuration.md cover both options; parser/onboarding/JSON/doctor/config/repo tests pass; sase just fmt, ruff, mypy, and symvision pass.

## Dependencies

- **Blocks:** [bob-cli-1w.2](bob-cli-1w.2.md) ◐ · ⧖ 2026-09-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-1w.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-1w.1/README.md) | [bob-cli-1w.1](bob-cli-1w.1.md) | 0 |
