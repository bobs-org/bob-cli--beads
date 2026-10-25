# Bead: bob-cli-c5.2 — The root\_parent dimension in bob stats

[Bead Pages](../README.md) / [bob-cli-c5](README.md) / bob-cli-c5.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.145](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.145.md) · **Assignee:** `bob-cli-c5.2` · **Size:** medium
**Created:** 2026-10-25 10:27:22 EDT · **Closed:** 2026-10-25 11:33:02 EDT
**Plan:** [202610/day\_strip\_above\_badges\_root\_parents.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/day_strip_above_badges_root_parents.md)

## Description

root-dimension: derive each home's root parent in the resolver and report an additive root_parent parts dimension and catalog field for Pomodoro and task metrics, with human output, tests, docs, and a performance check.

## Notes

[2026-10-25T15:33:02Z · bob-cli-c5.2] root_parent dimension shipped: resolver derives root per R2 algorithm, SessionSplit/catalog/metrics/render carry additive root_parent with labels/apportioned, H16 (sase 80, review 35, bob 10, dev 10, job 4, job_apply 3, unlinked 10, unfiled 15) plus apportioned/lead/catalog/week/golden/resolver tests pass; docs R2/R10/stats H16/perf updated; just check and docs-check green; perf after median 177.5ms vs before 179.1ms within 10%

## Dependencies

- **Depends on:** [bob-cli-c5.1](bob-cli-c5.1.md) ✓ · ⧖ 2026-10-25
- **Blocks:** [bob-cli-c5.4](bob-cli-c5.4.md) ◐ · ⧖ 2026-10-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-c5.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c5.2/README.md) | [bob-cli-c5.2](bob-cli-c5.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`5078e8f`](https://github.com/bobs-org/bob-cli/commit/5078e8f821652dd66d7b61ce131a61232d08a415) | feat(stats): add root\_parent dimension to pomodoro homes and stats | [bob-cli-c5.2](bob-cli-c5.2.md) | 2026-10-25 11:34:38 EDT |
