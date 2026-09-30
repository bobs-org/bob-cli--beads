# Bead: bob-cli-2r.2 — Report every remaining Pomodoro-touching capture

[Bead Pages](../README.md) / [bob-cli-2r](README.md) / bob-cli-2r.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.3c](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.3c.md) · **Assignee:** `bob-cli-2r.2` · **Size:** medium
**Created:** 2026-09-30 07:52:28 EDT · **Closed:** 2026-09-30 09:34:52 EDT
**Plan:** [202609/pomodoro\_full\_block\_preview.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/pomodoro_full_block_preview.md)

## Description

blocks_refs: add explicit refs for link and task starts, close link and task forms, Pomodoro task and link captures, and Ensure Next, including mention-only cases. Prove that toggles, Pomodoro notes, and project notes are auto-detected. Add a coverage-invariant test helper used by every Pomodoro CLI test family.

## Notes

[2026-09-30T13:34:26Z · bob-cli-2r.2] PROPOSED FOLLOW-UP: just lint deny failure in tests/cli/capture/pomodoro_name.rs:808 (overly_complex_bool_expr from `|| true`) reproduces identically on the clean base tree; fix or suppress it separately

[2026-09-30T13:34:39Z · bob-cli-2r.2] PROPOSED FOLLOW-UP: two-way toggle that MOVES a Task Link between entries at equal indentation (insert plus duplicate-removal netting to a pure line move) emits no pomodoro_blocks; Myers aligns the moved bytes and auto-detection deliberately ignores moves, and toggles carry no refs per the blocks_refs plan

[2026-09-30T13:34:52Z · bob-cli-2r.2] blocks_refs done: explicit started/linked refs for link/task starts (incl. link-with-start moves and mention-only already-current), closed/unlinked/next refs for close link and task forms, linked/unlinked refs for solo links and Ensure Next; toggles/Pomodoro notes/project notes proven auto-detected; assert_pomodoro_blocks_cover_changes helper wired into all 13 Pomodoro CLI test families; docs/capture.md notes blocks under link/toggle/ensure-next/note/project-note JSON. Verified: cargo fmt clean, full cargo test green (1297 lib + 624 cli + all integration suites, 0 failed), just lint fails only on the pre-existing pomodoro_name.rs:808 deny also present on the clean base (recorded on bead). No epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-2r.1](bob-cli-2r.1.md) ✓ · ⧖ 2026-09-30
- **Blocks:** [bob-cli-2r.4](bob-cli-2r.4.md) ✓ · ⧖ 2026-09-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2r.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2r.2/README.md) | [bob-cli-2r.2](bob-cli-2r.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a297a48`](https://github.com/bobs-org/bob-cli/commit/a297a48c4646f07a9f519bfcaad77d22045938a1) | feat(capture): report every remaining Pomodoro-touching capture in pomodoro\_blocks | [bob-cli-2r.2](bob-cli-2r.2.md) | 2026-09-30 09:39:18 EDT |
