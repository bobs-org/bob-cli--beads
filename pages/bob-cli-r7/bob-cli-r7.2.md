# Bead: bob-cli-r7.2 — Stale ignored mount index is not an authored landing page

[Bead Pages](../README.md) / [bob-cli-r7](README.md) / bob-cli-r7.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1h4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1h4.md) · **Assignee:** `bob-cli-r7.2` · **Size:** small
**Created:** 2026-11-27 10:16:12 EST · **Closed:** 2026-11-27 10:46:34 EST
**Plan:** [202611/task\_bead\_burndown\_1.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_bead_burndown_1.md)

## Description

docs-mount-index: stop bob-docs calling an untracked, gitignored mount index.md a committed landing page, add a tools/docs test, then close bob-cli-it.

## Notes

[2026-11-27T15:46:34Z · bob-cli-r7.2] docs-mount-index: untracked gitignored unmanifested mount copies are stale output and may be replaced; tracked/non-ignored landing pages still refuse. Tests added in tools/docs/tests/test_mounts.py. Verified: tools/docs pytest 449 passed 1 skipped; just docs-check passed with planted stale docs/reference/plugins/index.md (manifest removed) and again clean. Closed bob-cli-it. No --epic-symbol leftovers.

[2026-11-27T15:57:19Z · bob-cli-r7.2--1] PROPOSED FOLLOW-UP: just check clippy_gate fails on HEAD at clippy::question_mark src/native/prose/section_model.rs:924 and clippy::items_after_test_module src/native/prose/relocate.rs:813; identical on clean tree (r7.1 close note; qj.5.1 note #1). Recovery repaired both so host completion can land docs-mount-index. Owned by in-progress epic bob-cli-qj.5.1 (phases .2/.3 closed).

## Dependencies

- **Depends on:** [bob-cli-r7.1](bob-cli-r7.1.md) ✓ · ⧖ 2026-11-27
- **Blocks:** [bob-cli-r7.3](bob-cli-r7.3.md) ✓ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-r7.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-r7.2.md) | [bob-cli-r7.2](bob-cli-r7.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`1878531`](https://github.com/bobs-org/bob-cli/commit/187853158344f2978486c3d0164b4fe6f7040fd1) | fix(docs): replace stale gitignored mount copies instead of treating them as authored | [bob-cli-r7.2](bob-cli-r7.2.md) | 2026-11-27 11:24:24 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-r7.2--2][1] | Inspect assigned bead status, notes, and close vs keep | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-r7.2.md

<!-- sase:referenced-by:end -->
