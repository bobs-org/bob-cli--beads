# Bead: bob-cli-r8.4 — Stable task-wikilink cold-build 16 ms chunk measurement

[Bead Pages](../README.md) / [bob-cli-r8](README.md) / bob-cli-r8.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-r7.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-r7.land.md) · **Assignee:** `bob-cli-r8.4` · **Size:** medium
**Created:** 2026-11-27 13:01:15 EST · **Closed:** 2026-11-27 15:11:17 EST
**Plan:** [202611/task\_bead\_burndown\_2.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_bead_burndown_2.md)

## Description

wikilink-cold-chunk: make the block-id-prompt task-wikilink cold-build 16 ms chunk gate measure chunk cost instead of helper-thread and cold-start noise under the serial test:perf stage, keep every budget, then close bob-cli-f8.

## Notes

[2026-11-27T20:11:17Z · bob-cli-r8.4] wikilink-cold-chunk: closed bob-cli-f8. Helper-thread CPU noise (Node v22.14.0 process.cpuUsage, wall 2-3 ms) was failing the 16 ms gate at 16.1-18.3 ms; chunker was not overshooting. Test now warms code then best-of-7 cold indexes; all budgets kept. decisions:bob-cli-releases-ride-a-daily-train honored (test-only, no Cargo.toml/CHANGELOG, no plugin sync). Focused file 5/5. Three consecutive npm test runs passed this node at 8.46 / 9.59 / 9.80 ms CPU; only known snooze-add-resnooze-replaces-history failure (bob-cli-q5). test:perf 26/26. No --epic-symbol entries. Parent epic left open.

## Dependencies

- **Depends on:** [bob-cli-r8.3](bob-cli-r8.3.md) ✓ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-r8.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-r8.4/README.md) | [bob-cli-r8.4](bob-cli-r8.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@4eb201e`](https://github.com/bobs-org/bob-plugins/commit/4eb201ecf730dac950b9737d65ae61eb1eb22315) | test(block-id-prompt): stabilize wikilink cold-chunk 16ms gate | [bob-cli-r8.4](bob-cli-r8.4.md) | 2026-11-27 15:13:26 EST |
