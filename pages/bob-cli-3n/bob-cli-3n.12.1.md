# Bead: bob-cli-3n.12.1 — Fix R1-R10 reconcile correctness bugs in bob task-status-hooks

[Bead Pages](../README.md) / [bob-cli-3n.12](bob-cli-3n.12.md) / bob-cli-3n.12.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-3n.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-3n.land.md) · **Assignee:** `bob-cli-3n.12.1` · **Size:** medium
**Created:** 2026-10-02 23:24:08 EDT · **Closed:** 2026-10-02 23:45:26 EDT
**Plan:** [202610/task\_dep\_links\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_dep_links_fixes.md)

## Description

hooks-correctness: fix the reconcile edit ordering that duplicates task lines, the task-line rewrite merge, dropped current-daily edits, previous-daily writes, field placement before trailing tags, archived legacy children, and the silent unencodable target, and add the regression and missing CLI tests.

## Notes

[2026-10-03T03:45:26Z · bob-cli-3n.12.1] hooks-correctness done. Fixed reconcile.rs (same-index Replace/Remove-before-Insert ordering; pending-rewrite merge for chained task-line edits; previous-daily targets never stamped with previous_daily_target warning; unencodable targets warn unencodable_dependency_target and stay verbatim/unprojected; R1 drops warn dependency_field_ids_dropped; done/ legacy children follow 4.3; set_task_fields rebuilt on shared projects::edits helpers so trailing tags never duplicate fields), compose.rs daily fallback now writes reconciled contents, contract 4/S3/S4.1 document the three new warning kinds. Tests: 3 new field-writer unit tests; 12 new CLI regression tests in dependency_lines.rs (ordering repro, chain one-run settlement, daily adoption+stamp, previous-daily, trailing tags, archive legacy x2 paths, unencodable, unblock-on-remove, breadcrumb+heal, quiet-interval deferral, cross-note stamp, legacy window) each asserting a clean second run; verified the 3 key tests fail on pre-fix sources. just all passes (fmt+clippy+full suite, 25/25 dependency_lines). Real-vault dry-run: 4632 files, 0 projections/adoptions/heals/canonicalizations/warnings (no Depends-On usage yet, nothing for the Mac cron to write). No epic-symbol leftovers.

## Dependencies

- **Blocks:** [bob-cli-3n.12.2](bob-cli-3n.12.2.md) ◐ · ⧖ 2026-10-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3n.12.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3n.12.1/README.md) | [bob-cli-3n.12.1](bob-cli-3n.12.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8d54b0e`](https://github.com/bobs-org/bob-cli/commit/8d54b0e6ad9dc9ae7d0412b9e2e29c4fb7a99d25) | fix(task-status-hooks): reconcile correctness for dependency lines | [bob-cli-3n.12.1](bob-cli-3n.12.1.md) | 2026-10-02 23:46:42 EDT |
