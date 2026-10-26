# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.4 — Open a new Stats tab on a modified Day strip click even when Stats is open

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.4` · **Size:** small
**Created:** 2026-10-26 08:32:07 EDT · **Closed:** 2026-10-26 09:14:49 EDT
**Plan:** [202610/backlog\_batch12\_perf\_baseline\_fakenode\_daystrip\_blocks\_notice.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch12_perf_baseline_fakenode_daystrip_blocks_notice.md)

## Description

day-strip-new-tab: resolve bob-cli-c6 by making openStatsForDay skip the reuse branch for newLeaf requests, with a host test, the docs/stats.md wording fix, and a bob plugins sync deploy.

## Notes

[2026-10-26T13:14:49Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.4] Verified openStatsForDay opens a new leaf for newLeaf=true even when Stats is already open, preserves pinned day and metric, and still reuses the existing leaf for plain clicks. Passed focused host tests (31/31), npm test (3,685 passed), npm run validate (7/7 plugins valid), and just docs-check (all implemented gates passed; 447 passed, 1 optional font test skipped). Deployed with bob plugins sync --repo; bob plugins list reports bob-ledger-tools 1.72.0 synced.

## Dependencies

- **Depends on:** [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.2](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.2.md) ✓ · ⧖ 2026-10-26
- **Depends on:** [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.3](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.3.md) ✓ · ⧖ 2026-10-26
- **Blocks:** [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.5](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.5.md) ◐ · ⧖ 2026-10-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.4/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.4](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`3633a10`](https://github.com/bobs-org/bob-cli/commit/3633a10a51dbaa0c5d05f2509ec3f9806b98b045) | docs(stats): clarify Day strip new-tab behavior | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.4](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.4.md) | 2026-10-26 09:15:40 EDT |
