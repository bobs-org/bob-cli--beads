# Bead: bob-cli-4i.4 — Execute \`!note:block-id\` through the engine with rich JSON and human output

[Bead Pages](../README.md) / [bob-cli-4i](README.md) / bob-cli-4i.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.5a](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.5a.md) · **Assignee:** `bob-cli-4i.4` · **Size:** medium
**Created:** 2026-10-05 15:13:24 EDT · **Closed:** 2026-10-05 16:06:40 EDT
**Plan:** [202610/bang\_task\_complete.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bang_task_complete.md)

## Description

execute: in bob-cli, plan `TaskComplete` items through the staged batch writer. Resolve the note vault-wide, validate status and recurrence, then run the engine (tree close, scoped ledger retirement, dependent recovery). Emit kind `task_complete` with the `task_complete` object and placement `completed`, report task_blocks roles `completed`/`unblocked`, and print green human output. Update `bob capture --help`, docs/capture.md, README, and CLI tests.

## Notes

[2026-10-05T20:06:17Z · bob-cli-4i.4] PROPOSED FOLLOW-UP: just test lib failures reproduce identically on clean base (verified via git stash): completion::kinds::every_value_arg_has_a_decision (highlights create:audio lacks kinds decision; already tracked per bob-cli-4i.2 note #1) and capture_pomodoros::missing_note_and_missing_section_are_warning_successes (expects 0 warnings, gets 1); needs its own bead

[2026-10-05T20:06:23Z · bob-cli-4i.4] PROPOSED FOLLOW-UP: just lint deny clippy::overly_complex_bool_expr in tests/cli/capture/pomodoro_name.rs:808 (tautological || true); file untouched by this phase, pre-existing (already tracked per bob-cli-4i.1 note #3 and bob-cli-4i.2 note #2)

[2026-10-05T20:06:30Z · bob-cli-4i.4] SANDBOX CHECK (fixture vault copy, BOB_NOW=2026-10-05 09:30:00, NO_COLOR=1): `bob capture -b $V -- '!sase:fix-flaky'` on running CAPTURE holding [[sase#^fix-flaky]] printed: `✓ completed [*] → [x] Fix flaky gkeep test  sase.md ^fix-flaky` + `ledger  Task Link struck · 20261005.md`; sase.md now `- [x] #task Fix flaky gkeep test  [completion:: 2026-10-05] ^fix-flaky`, link struck in place; follow-up `bob task reconcile` reported no ledger/status changes for the completed task.

[2026-10-05T20:06:40Z · bob-cli-4i.4] Execute done and verified: staged batch writer replaces temp refusal; kind task_complete + placement completed + task_complete object (action/subtasks/left-open/ledger/unblocked), task_blocks completed/unblocked roles, green human output with done-green x. Verified: cargo fmt --check clean; 13 new CLI tests + 7 parse tests green; full CLI suite 984 passed; lib 1699 passed except 2 failures proven identical on clean base (recorded as follow-ups); clippy red only on pre-existing pomodoro_name deny (recorded). Manual sandbox human output pasted in bead notes. No epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-4i.1](bob-cli-4i.1.md) ✓ · ⧖ 2026-10-05
- **Depends on:** [bob-cli-4i.2](bob-cli-4i.2.md) ✓ · ⧖ 2026-10-05
- **Blocks:** [bob-cli-4i.5](bob-cli-4i.5.md) ◐ · ⧖ 2026-10-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-4i.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-4i.4/README.md) | [bob-cli-4i.4](bob-cli-4i.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`fbc4f43`](https://github.com/bobs-org/bob-cli/commit/fbc4f4399cf4aae1130218c9092d172dbf95b683) | feat(capture): execute whole-item !note:block-id completions | [bob-cli-4i.4](bob-cli-4i.4.md) | 2026-10-05 16:07:56 EDT |
