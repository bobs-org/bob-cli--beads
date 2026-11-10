# Bead: bob-cli-j5.5 — Keep window and month headings

[Bead Pages](../README.md) / [bob-cli-j5](README.md) / bob-cli-j5.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1ai](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1ai.md) · **Assignee:** `bob-cli-j5.5` · **Size:** medium
**Created:** 2026-11-09 11:04:08 EST · **Closed:** 2026-11-09 23:40:50 EST
**Plan:** [202611/done\_notes\_archiving\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/done_notes_archiving_fixes.md)

## Description

keep-window: replace the count gate with the chosen keep window, keep -t as an optional minimum batch, file new roots under close-month headings, and confirm the rule with a read-only live-vault dry run.

## Notes

[2026-11-10T04:40:00Z · bob-cli-j5.5] PROPOSED FOLLOW-UP: Fix the pre-existing mg18 bound archive assertion — clean-base cargo test reproduces native::task_merge::tests::mg18_merge_source_with_descendant_anchor_archives_through_bound_pair failing because the planner writes done/src_done while the test expects done/custom_archive.

[2026-11-10T04:40:13Z · bob-cli-j5.5] PROPOSED FOLLOW-UP: Resolve the baseline docs assembly collision — just docs-check reports bob-mac-capture source index.md colliding with committed docs/reference/mac-capture/index.md; both collision inputs are untouched by this phase.

[2026-11-10T04:40:50Z · bob-cli-j5.5] Implemented the trailing-week keep window with a 10-root recent cap, close-month archive headings, optional minimum batch, and schema v2 docs. Verified 154 archive tests, 24 archive CLI tests, cargo fmt, diff check, docs generation, and a read-only live-vault preview (dry_run=true; 38 planned moves). Full just check has one task-merge test failure reproduced identically on the clean base; recorded as a proposed follow-up. just docs-check also hits the unchanged bob-mac-capture index mount collision; recorded as a proposed follow-up.

## Dependencies

- **Depends on:** [bob-cli-j5.4](bob-cli-j5.4.md) ✓ · ⧖ 2026-11-09
- **Blocks:** [bob-cli-j5.7](bob-cli-j5.7.md) ✓ · ⧖ 2026-11-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-j5.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-j5.5/README.md) | [bob-cli-j5.5](bob-cli-j5.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`15a7999`](https://github.com/bobs-org/bob-cli/commit/15a79998ebee433dd2bd3dc76b1e3dc4c5ba0ab1) | feat(archive)!: keep window and group archived closures by month | [bob-cli-j5.5](bob-cli-j5.5.md) | 2026-11-10 00:03:43 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-j5.5][1] | Need the phase scope, design file, and prior work notes before implementation | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-j5.5/README.md

<!-- sase:referenced-by:end -->
