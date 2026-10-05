# Bead: bob-cli-4i.7.2 — Picker status filter, today-section sinking, and parse/claim consistency

[Bead Pages](../README.md) / [bob-cli-4i.7](bob-cli-4i.7.md) / bob-cli-4i.7.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-4i.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-4i.land.md) · **Assignee:** `bob-cli-4i.7.2` · **Size:** small
**Created:** 2026-10-05 18:10:31 EDT · **Closed:** 2026-10-05 18:22:09 EDT
**Plan:** [202610/bang\_task\_complete\_finish.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bang_task_complete_finish.md)

## Description

picker_parse: in bob-cli, limit the completable-task catalog to ` `/`?`/`*`/`/` tasks, sink hidden and recurring rows inside each today entry, mirror the `task_complete` object at the top level of single-item capture-parse JSON, and claim `!` before dependency scanning in execution. Fill the grammar/picker test gaps. Fix the stale capture-parse and capture-complete reference lists in docs/capture.md.

## Notes

[2026-10-05T22:22:09Z · bob-cli-4i.7.2] picker_parse done: shared is_completable_status (catalog+execute), canonical_key sinks hidden/recurring within each today entry, top-level task_complete on single-item capture-parse, ! claim before dep scan. Tests: 486 capture CLI + 272 capture_language lib pass; fmt clean; clippy shows only pre-existing bob-cli-28 deny; kinds test fails as expected per bob-cli-4j.

## Dependencies

- **Blocks:** [bob-cli-4i.7.3](bob-cli-4i.7.3.md) ✓ · ⧖ 2026-10-05
- **Blocks:** [bob-cli-4i.7.4](bob-cli-4i.7.4.md) ◐ · ⧖ 2026-10-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-4i.7.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-4i.7.2/README.md) | [bob-cli-4i.7.2](bob-cli-4i.7.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`3fbfb7b`](https://github.com/bobs-org/bob-cli/commit/3fbfb7b7e5a720b802fec36a9ce87037842f690a) | feat(capture): picker status filter, today sinking, and parse/claim consistency | [bob-cli-4i.7.2](bob-cli-4i.7.2.md) | 2026-10-05 18:23:16 EDT |
