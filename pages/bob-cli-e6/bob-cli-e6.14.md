# Bead: bob-cli-e6.14 — Note moves and Pomodoro renames keep agreement

[Bead Pages](../README.md) / [bob-cli-e6](README.md) / bob-cli-e6.14

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2t.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2t.linker.w0.md) · **Assignee:** `bob-cli-e6.14` · **Size:** medium
**Created:** 2026-10-29 16:16:34 EDT · **Closed:** 2026-10-30 01:00:22 EDT
**Plan:** [202610/task\_types.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_types.md)

## Description

gesture-retype: relocate the live link when a note move changes an inherited type, and retype linked tasks when naming or renaming an entry gives it a different type.

## Notes

[2026-10-30T04:59:52Z · bob-cli-e6.14] PROPOSED FOLLOW-UP: plugin deploy blocked — `bob plugins sync` refuses to overwrite vault bob-navigation-hotkeys built from uncommitted sibling checkout bob-cli_16 (a42de4d); coordinate with that checkout owner or force-sync with -F, then verify D10 toast live.

[2026-10-30T04:59:57Z · bob-cli-e6.14] PROPOSED FOLLOW-UP: `test-navigation-task-card-view.cjs` grey-pill test (`theme menu stays grey when hueFor is missing`) fails identically on the clean base tree (verified via stash); pre-existing, unrelated to gesture-retype.

[2026-10-30T05:00:12Z · bob-cli-e6.14] PROPOSED FOLLOW-UP: entry-rename picker has no `3 tasks become BUILD` type preview line and no new Node harness tests for `planNoteMoveLedgerRelocation`/rename-retype; commit applies retype with D12 recheck plus toast suffix, picker preview plus harness tests remain.

[2026-10-30T05:00:22Z · bob-cli-e6.14] gesture-retype done, both halves. Rust: task_move relocation (relocated[], strict_cap refusal aborts) plus capture-pomodoro-name retype (retyped[], container/label skip, repair skip), both new tests pass, clippy gate clean. Obsidian: 655 planNoteMoveLedgerRelocation merges daily link relocation into plan.changes with D8 field/effective checks plus 650 D10 toast suffix; 650 entry-rename retype via fresh preview, D12 recheck, local plus group writes, type toast suffix; fragments under 1000 lines, node syntax OK, npm run build clean, 89/89 move/pomodoro plugin tests pass, 2/2 new Rust tests pass. Full plugin suite 4369/4370 with one grey-pill failure proven pre-existing on clean base (follow-up noted). Deploy blocked by sibling bob-cli_16 uncommitted build (follow-up noted); picker preview line plus harness tests remain (follow-up noted). Epic-symbols clean.

## Dependencies

- **Depends on:** [bob-cli-e6.13](bob-cli-e6.13.md) ✓ · ⧖ 2026-10-29
- **Blocks:** [bob-cli-e6.16](bob-cli-e6.16.md) ◐ · ⧖ 2026-10-29
- **Depends on:** [bob-cli-e6.7](bob-cli-e6.7.md) ✓ · ⧖ 2026-10-29
- **Depends on:** [bob-cli-e6.9](bob-cli-e6.9.md) ✓ · ⧖ 2026-10-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-e6.14](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-e6.14/README.md) | [bob-cli-e6.14](bob-cli-e6.14.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`785c1ae`](https://github.com/bobs-org/bob-cli/commit/785c1aecbf62b999fdc4b3797df971eee91d3e26) | feat(task-move,capture): gesture-retype keeps agreement on note moves and Pomodoro renames | [bob-cli-e6.14](bob-cli-e6.14.md) | 2026-10-30 01:19:19 EDT |
| bob-plugins | [`bob-plugins@8b262bb`](https://github.com/bobs-org/bob-plugins/commit/8b262bb92c16e5b886c32ab7b5adb0430e1a82a8) | feat(navigation-hotkeys): relocate live Task Link on note moves, retype on Pomodoro renames | [bob-cli-e6.14](bob-cli-e6.14.md) | 2026-10-30 01:24:26 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-e6.14][1] | check full scope | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-e6.14/README.md

<!-- sase:referenced-by:end -->
