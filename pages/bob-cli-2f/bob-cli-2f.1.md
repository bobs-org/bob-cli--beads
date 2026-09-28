# Bead: bob-cli-2f.1 — Split tests/cli.rs

[Bead Pages](../README.md) / [bob-cli-2f](README.md) / bob-cli-2f.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.2u](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.2u.md) · **Assignee:** `bob-cli-2f.1` · **Size:** large
**Created:** 2026-09-28 16:49:29 EDT · **Closed:** 2026-09-28 17:20:55 EDT
**Plan:** [202609/split\_largest\_rust\_files.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/split_largest_rust_files.md)

## Description

split-cli-tests: turn the 35k-line CLI integration test file into a single `tests/cli/` test target with a shared support module and per-command test modules, each at most 1500 lines.

## Notes

[2026-09-28T21:20:30Z · bob-cli-2f.1] PROPOSED FOLLOW-UP: Eliminate pre-existing clippy::overly_complex_bool_expr on preserved || true in capture_pomodoro_link_solo_grammar test (source line 31821 in HEAD, now tests/cli/capture/pomodoro_name.rs:811) — cited against bob-cli-28 and bob-cli-v, reproduces from HEAD, tracked under bob-cli-v

[2026-09-28T21:20:55Z · bob-cli-2f.1] Split tests/cli.rs (35334 lines, 515 tests) into single cli target at tests/cli/main.rs with shared support and per-command modules, all <=1500 lines (max 1173).

Verification:
- Baseline before: wc -l 35334, 515 #[test], cargo test --test cli -- --list 515. After: rg sums 515, list 515, match.
- find tests/cli -name '*.rs' shows no file over 1500, tests/cli.rs gone.
- cargo package --list --allow-dirty lists all 53 files under tests/cli/.
- cargo fmt --check passes. cargo clippy reports no new warnings; only pre-existing deny clippy::overly_complex_bool_expr on preserved || true (HEAD:31821, now capture/pomodoro_name.rs:811, cited bob-cli-28 and bob-cli-v, reproduces from HEAD) plus pre-existing unnecessary_to_owned warning also in HEAD (30769-30770). Preserved || true unchanged, no #[allow] added.
- cargo test --test cli: 515 passed. cargo test (all targets): pass.
- tests/randomize.rs comments updated to tests/cli/support.rs and support.rs::init_vault_sync_pair; rg tests/cli.rs clean.
- include_str rewritten to ../../fixtures in nested modules.
- sase bead epic-symbols bob-cli-2f.1: none.
- projects/sync has 13 tests (not table 15); table summed to 517, actual 515 all assigned, difference is that overcount.
- Shared helpers: support.rs holds >=2-module helpers (pub(crate)); priority helpers pub(crate) in capture/priority.rs with super::priority import in project_note/sub_bullet/authored; close helpers pub(crate) in capture/pomodoro_close.rs with super import in whole_item; capture_pomodoro_ref moved to support (needed by task_id via capture_task_ref and pomodoro_name); LegacyHelpCase private in help.rs; TempDir new/path pub(crate).

Files (lines, contents):
- tests/cli/main.rs (14): //! + mod declarations only.
- tests/cli/support.rs (618): shared helpers, consts, TempDir, 0 tests.
- tests/cli/help.rs (984): 25 cache/native/legacy/script/top-level/nightly help.
- tests/cli/help_options.rs (681): 20 alphabetical listings.
- tests/cli/task_status_hooks/sync.rs (1150): 6 fixture sync/grouping/rank/prune.
- tests/cli/task_status_hooks/structure.rs (939): 10 empty pomodoros/guardrails/archives/strike/compose.
- tests/cli/task_status_hooks/blocked.rs (481): 5 blocked/schedules/recovery.
- tests/cli/task_status_hooks/retry.rs (663): 10 lock/retry/cron.
- tests/cli/dataview.rs (1017): 18 dataview behavior.
- tests/cli/projects/list.rs (194): 2 projects_list.
- tests/cli/projects/sync.rs (965): 13 remaining projects_sync.
- tests/cli/projects/schedule.rs (336): 5 exact schedule tail.
- tests/cli/plugins.rs (639): 13 plugins behavior.
- tests/cli/highlights/create.rs (560): 11 highlights_create.
- tests/cli/highlights/scan_hooks.rs (481): 10 pre-scan hooks.
- tests/cli/highlights/scan.rs (1000): 15 other scans.
- tests/cli/highlights/sync.rs (474): 9 marker sync guards.
- tests/cli/highlights/sync_tasks.rs (1141): 11 sidecar/annotation routing.
- tests/cli/highlights/tasks.rs (1119): 10 task/status.
- tests/cli/highlights/marker.rs (1097): 16 remaining refs.
- tests/cli/move_done.rs (930): 11 move_done.
- tests/cli/pomodoro.rs (243): 10 pomodoro/tmux/script.
- tests/cli/vault_sync.rs (902): 17 vault_sync/conflict/renamed/nightly/stubs.
- tests/cli/capture/parse.rs (1055): 24 parse except pomodoro protocol.
- tests/cli/capture/parse_pomodoro.rs (936): 7 parse pomodoro.
- tests/cli/capture/rewrite.rs (368): 12 rewrite + and-rewrite.
- tests/cli/capture/complete_query.rs (684): 12 completion query.
- tests/cli/capture/complete_editor.rs (954): 18 completion editor.
- tests/cli/capture/project_note.rs (634): 6 project_note.
- tests/cli/capture/priority.rs (578): 12 priority + 3 helpers.
- tests/cli/capture/task_marker.rs (216): 5 block-id/retired.
- tests/cli/capture/task_toggle.rs (520): 5 toggle except ensure-next.
- tests/cli/capture/ensure_next.rs (703): 4 ensure-next.
- tests/cli/capture/batch.rs (451): 11 batch + global.
- tests/cli/capture/clip.rs (1068): 15 clip/history/clipboard/percent.
- tests/cli/capture/authored.rs (696): 19 authored.
- tests/cli/capture/sub_bullet.rs (734): 7 sub-bullet.
- tests/cli/capture/bare.rs (433): 11 bare terminal.
- tests/cli/capture/sections.rs (1040): 14 forced/task-section/sections/tasks.
- tests/cli/capture/targets.rs (238): 5 targets.
- tests/cli/capture/task_id.rs (519): 4 task-id/sections.
- tests/cli/capture/routing.rs (879): 26 remaining routing.
- tests/cli/capture/pomodoro_link.rs (556): 9 linked/named execution.
- tests/cli/capture/pomodoro_name.rs (1053): 8 pomodoros/name/human/link-solo.
- tests/cli/capture/pomodoro_start.rs (1021): 15 start.
- tests/cli/capture/pomodoro_whole_item.rs (1147): 6 whole-item.
- tests/cli/capture/pomodoro_adjust.rs (526): 5 adjust.
- tests/cli/capture/pomodoro_shift.rs (792): 5 shift.
- tests/cli/capture/pomodoro_close.rs (1173): 3 close + 3 helpers.
- Plus 4 mod.rs index files (capture 28, highlights 9, projects 5, task_status_hooks 6) with //! + mod lines only.

## Dependencies

- **Blocks:** [bob-cli-2f.2](bob-cli-2f.2.md) ✓ · ⧖ 2026-09-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2f.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-2f.1.md) | [bob-cli-2f.1](bob-cli-2f.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`7d1c8dd`](https://github.com/bobs-org/bob-cli/commit/7d1c8dd3054fd30f6e4f5a15e2dc61c42c3b2593) | refactor(tests): split tests/cli.rs into tests/cli/ target with support and per-command modules | [bob-cli-2f.1](bob-cli-2f.1.md) | 2026-09-28 17:22:16 EDT |
