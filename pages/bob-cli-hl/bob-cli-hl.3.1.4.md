# Bead: bob-cli-hl.3.1.4 — Complete pending context, merge copy, and stdin redirect refusal

[Bead Pages](../README.md) / [bob-cli-hl.3.1](bob-cli-hl.3.1.md) / bob-cli-hl.3.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-hl.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hl.3.md) · **Assignee:** `bob-cli-hl.3.1.4` · **Size:** medium
**Created:** 2026-11-05 19:49:42 EST · **Closed:** 2026-11-05 22:08:29 EST
**Plan:** [202611/capture\_merge\_in\_execution.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_merge_in_execution.md)

## Description

feedback: implement merge_in_pending, fd-0 shell protection, existing-merge teaching copy, the new-target human header, and bob-cli-hi G2/G4/G5 with the approved pruned-source title count.

## Notes

[2026-11-06T03:08:10Z · bob-cli-hl.3.1.4] PROPOSED FOLLOW-UP: Pre-existing just-check failures reproduce on clean base — help::root_help snapshot, catalog protocol_1 (73 vs 72) and public_leaves, completion kinds duplicate clipboard:count, 5x note_pull fixture tests (np1 np2 np13 np16 np_move_groups); verified via git stash -u on this checkout

[2026-11-06T03:08:13Z · bob-cli-hl.3.1.4] PROPOSED FOLLOW-UP: Pre-existing docs-check lychee failure — task-merge/index.html links target/docs/capture#merging-tasks-into-a-new-task-with as missing file; docs/ untouched by this phase so not caused here

[2026-11-06T03:08:29Z · bob-cli-hl.3.1.4] Feedback done: merge_in_pending attach (dry-run JSON item/need/sources with mergeability, list+balk item lookup, commit/human omission), fd-0 stdin shell_ate_merge_in_arrow guard with argv gating (stdout guard preserved, CLI help + docs/reference/cli/capture.md regen), merge_source_closed teaching copy naming S/T/note (both plan + retirement sites, unit test), new-target human header with singular + existing-task wording kept (G2 label merges print once with relations retained), G4 singular 1 note moved (plan + test helper), G5 pruned-source title count (transfer test updated to single-qualifying-source title). Gates: cargo fmt clean, cargo clippy gate exit 0, lib task_merge 52 passed, lib capture 388 passed, CLI merge_in 12 + relations_merge 5 + transfer 30 passed, docs_reference passes post-regen; full just-check/docs-check failures reproduce identically on clean base (recorded as PROPOSED FOLLOW-UP, docs/ untouched).

## Dependencies

- **Depends on:** [bob-cli-hl.3.1.2](bob-cli-hl.3.1.2.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hl.3.1.5](bob-cli-hl.3.1.5.md) ✓ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-hl.3.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hl.3.1.4/README.md) | [bob-cli-hl.3.1.4](bob-cli-hl.3.1.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`fbb6da4`](https://github.com/bobs-org/bob-cli/commit/fbb6da46fdfff73a1b358e7087336806498a247c) | feat(capture): complete merge-in feedback — pending context, copy, and stdin guard | [bob-cli-hl.3.1.4](bob-cli-hl.3.1.4.md) | 2026-11-05 22:09:59 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hl.3.1.4][1] | Need the phase scope and design file | 3 |
| read-by | [agent:bob-cli-hl.3.1.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hl.3.1.4/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hl.3.1.land/README.md

<!-- sase:referenced-by:end -->
