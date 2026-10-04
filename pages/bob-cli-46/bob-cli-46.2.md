# Bead: bob-cli-46.2 — bob task and bob pomodoro groups with permanent aliases

[Bead Pages](../README.md) / [bob-cli-46](README.md) / bob-cli-46.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.4y](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.4y.md) · **Assignee:** `bob-cli-46.2` · **Size:** medium
**Created:** 2026-10-04 07:02:06 EDT · **Closed:** 2026-10-04 08:54:43 EDT
**Plan:** [202610/bob\_command\_tree.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_command_tree.md)

## Description

command-groups: add Leaf/Group targets to the runner table, route `bob task` and `bob pomodoro` (bare = status), map the five old names onto canonical paths as silent aliases, print canonical names in every leaf's help, diagnostics, logs, and commit subjects, mount the groups in completion, and add alias-parity, routing, and help snapshot tests.

## Notes

[2026-10-04T12:31:23Z · bob-cli-46.2] Implemented Leaf/Group runner table, five silent aliases (mark-next-tasks/task-status-setter/task-status-hooks→task reconcile, move-done-tasks→task archive, randomize→task reroll, notify→pomodoro notify, tmux-pomodoro→pomodoro tmux), canonical COMMAND_NAMEs, group default insertion (bare task=help exit 2; bare pomodoro=status), completion group mount, alias-parity/help snapshots, install-smoke canonical --help. vault_sync::run_notify still argv bob notify. epic-symbols: none leftover. Closing after just all && just install-smoke.

[2026-10-04T12:36:23Z · bob-cli-46.2--1] PROPOSED FOLLOW-UP: just lint fails on clean master with deny-by-default clippy::overly_complex_bool_expr at tests/cli/capture/pomodoro_name.rs:808-811 (assert ends in || true; git blame 7d1c8dd split of bob-cli-28.1 solo-link test). Reproduced by just all on this phase tree; file is unmodified vs HEAD 660c171. In-progress epic bob-cli-28 owns the closeout; bob-cli-v tracks warnings only. No task bead tracks this deny.

[2026-10-04T12:51:16Z · bob-cli-46.2--3] PROPOSED FOLLOW-UP: just test flakes on unmodified native::capture_pomodoros::tests::missing_note_and_missing_section_are_warning_successes (assert_eq missing.count 0 got 1 at capture_pomodoros.rs:1196) under parallel cargo test; isolated --exact passes. Tracked by bob-cli-2e (serialize BOB_DAY_FILE) and flake bob-cli-40. Reproduced on this phase tree; file unmodified vs HEAD 660c171.

[2026-10-04T12:54:43Z · bob-cli-46.2--3] Nested bob task {archive,reconcile,reroll} and bob pomodoro {notify,status,tmux} groups with five silent aliases (mark-next-tasks/task-status-setter/task-status-hooks→task reconcile, move-done-tasks→task archive, randomize→task reroll, notify→pomodoro notify, tmux-pomodoro→pomodoro tmux). Canonical COMMAND_NAMEs in help/diagnostics/logs/commit subjects. Bare task=help exit 2; bare pomodoro=status. Completion mounts groups. Alias-parity, group-help snapshots, routing tests, and randomize top-level help now list task/reroll. install-smoke covers canonical --help. vault_sync::run_notify still argv bob notify. Verified: just fmt; cargo test --lib runner::, --test cli aliases, --test randomize; just install-smoke. just test failed on pre-existing capture_pomodoros BOB_DAY_FILE flake (bob-cli-2e / bob-cli-40; isolated --exact passes; +1 on bob-cli-2e). just lint still fails on pre-existing pomodoro_name.rs:808 || true clippy deny (bob-cli-28). epic-symbols: none leftover. Did not close parent epic bob-cli-46.

## Dependencies

- **Depends on:** [bob-cli-46.1](bob-cli-46.1.md) ✓ · ⧖ 2026-10-04
- **Blocks:** [bob-cli-46.3](bob-cli-46.3.md) ◐ · ⧖ 2026-10-04
- **Blocks:** [bob-cli-46.4](bob-cli-46.4.md) ✓ · ⧖ 2026-10-04

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-46.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-46.2.md) | [bob-cli-46.2](bob-cli-46.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b13f96c`](https://github.com/bobs-org/bob-cli/commit/b13f96ccfbfdaac8c06e20c0b343f0f5cce7de60) | feat(cli): nest task and pomodoro command groups | [bob-cli-46.2](bob-cli-46.2.md) | 2026-10-04 08:56:02 EDT |
