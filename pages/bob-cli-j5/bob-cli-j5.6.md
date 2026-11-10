# Bead: bob-cli-j5.6 — bob task restore

[Bead Pages](../README.md) / [bob-cli-j5](README.md) / bob-cli-j5.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1ai](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1ai.md) · **Assignee:** `bob-cli-j5.6` · **Size:** medium
**Created:** 2026-11-09 11:04:09 EST · **Closed:** 2026-11-09 23:32:11 EST
**Plan:** [202611/done\_notes\_archiving\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/done_notes_archiving_fixes.md)

## Description

restore: let the task-move engine take a done/ source and add a thin bob task restore that defaults to the bound source, optionally reopens, and refuses recurring occurrences, merge tombstones, and ^prj lines.

## Notes

[2026-11-10T03:53:49Z · bob-cli-j5.6] PROPOSED FOLLOW-UP: just docs-check fails on clean master with mount bob-mac-capture -> reference/mac-capture collision (source ships index.md vs committed docs/reference/mac-capture/index.md, git-tracked since a8f61375); reproduced identically in a clean HEAD worktree, so pre-existing and unrelated to restore. Related but distinct from bob-cli-it (there the index is untracked+gitignored stale output; here it is tracked). Needs a mounts fix: either own the landing page or drop it from the mount.

[2026-11-10T04:12:47Z · bob-cli-j5.6] PROPOSED FOLLOW-UP: lib test native::task_merge::tests::mg18_merge_source_with_descendant_anchor_archives_through_bound_pair fails on clean master (verified via git stash): archive planner repairs merged-from links to the filename-guess done/src_done instead of the bound done/custom_archive. Pre-existing pairing/planner issue, unrelated to restore; needs a pairing-phase owner.

[2026-11-10T04:32:11Z · bob-cli-j5.6] bob task restore ships: engine restore mode (done/ sources, bound-source default, recurring/tombstone/prj refusals, --reopen, emptied month-heading trim) reusing the move pipeline; registered in task group, completion, catalog-excluded, golden CLI/help snapshots updated; 19 new tests green; just fmt/lint/test pass except pre-existing mg18 (clean-tree verified, PROPOSED FOLLOW-UP noted) and pre-existing docs-check mac-capture mount collision (clean-tree verified, PROPOSED FOLLOW-UP noted, related bob-cli-it). No epic symbols left.

## Dependencies

- **Depends on:** [bob-cli-j5.4](bob-cli-j5.4.md) ✓ · ⧖ 2026-11-09
- **Blocks:** [bob-cli-j5.7](bob-cli-j5.7.md) ◐ · ⧖ 2026-11-09
- **Blocks:** [bob-cli-j5.8](bob-cli-j5.8.md) ◐ · ⧖ 2026-11-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-j5.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-j5.6/README.md) | [bob-cli-j5.6](bob-cli-j5.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e5b0898`](https://github.com/bobs-org/bob-cli/commit/e5b0898e51670d39fe99fb959495ac7d12e37d3f) | feat(task-restore): add bob task restore over the task-move engine | [bob-cli-j5.6](bob-cli-j5.6.md) | 2026-11-09 23:34:10 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-j5.6][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-j5.6/README.md

<!-- sase:referenced-by:end -->
