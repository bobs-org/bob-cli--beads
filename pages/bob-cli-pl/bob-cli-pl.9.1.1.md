# Bead: bob-cli-pl.9.1.1 — Gate home-card Properties ownership and route native entry points

[Bead Pages](../README.md) / [bob-cli-pl.9.1](bob-cli-pl.9.1.md) / bob-cli-pl.9.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pl.9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pl.9.md) · **Assignee:** `bob-cli-pl.9.1.1` · **Size:** medium
**Created:** 2026-11-25 19:49:46 EST · **Closed:** 2026-11-25 20:18:10 EST
**Plan:** [202611/area\_project\_takeover.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/area_project_takeover.md)

## Description

home-ownership: extend the shared capability and mount coordinator for area/project cards, preserve fail-open behavior, and route summary/Add actions to the existing Property Editor.

## Notes

[2026-11-26T01:17:53Z · bob-cli-pl.9.1.1] PROPOSED FOLLOW-UP: test-task-status-cycler-open-line.cjs has 2 date-boundary failures (created::2026-11-26 vs 2026-11-25, Vim o/O + empty-scaffold prune) that reproduce identically on the clean base tree; unrelated to home-ownership, needs a date-stable fixture

[2026-11-26T01:18:10Z · bob-cli-pl.9.1.1] home-ownership landed: 298v tracks props_contract_v1 per bob path via lifecycle __catalog probe (confirmed/absent) plus typed-note show evidence (ordinary notes never downgrade); 240q gates area/project mounts on the contract with data-home-source mounts while album/record/bank keep generic props_v1; 249d routes connected home mounts through the coordinator with generation-bound release in Live/Reading/widget paths, row fallback limited to card-represented keys, native restored on any loss; summary/Add entry points route via openPropertyEditor setting summary. Verified: build+build:check, docs inventory, manifest validate, 329 focused tests green, test:unit 9712/9719 (2 pre-existing date-boundary failures reproduced on clean tree), test:perf 26 green, offline smoke self-test pass, bob plugins sync deployed (1 copied). Real-Obsidian matrix deferred to takeover-acceptance (no xvfb/obsidian here).

## Dependencies

- **Blocks:** [bob-cli-pl.9.1.2](bob-cli-pl.9.1.2.md) ◐ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pl.9.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pl.9.1.1/README.md) | [bob-cli-pl.9.1.1](bob-cli-pl.9.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@8698046`](https://github.com/bobs-org/bob-plugins/commit/8698046c10872ccde3e3a3c185e2447d3bcf24ed) | feat(ledger-tools): per-path props contract routing with home ownership and entry routing | [bob-cli-pl.9.1.1](bob-cli-pl.9.1.1.md) | 2026-11-25 20:19:22 EST |
