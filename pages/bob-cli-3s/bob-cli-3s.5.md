# Bead: bob-cli-3s.5 — Split plugin management into focused modules

[Bead Pages](../README.md) / [bob-cli-3s](README.md) / bob-cli-3s.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0vn](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0vn.md) · **Assignee:** `bob-cli-3s.5` · **Size:** large
**Created:** 2026-10-03 05:16:50 EDT · **Closed:** 2026-10-03 07:25:50 EDT
**Plan:** [202610/split\_largest\_rust\_files.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/split_largest_rust_files.md)

## Description

split-plugins: After split-capture-clip, reinspect src/native/plugins.rs and plan its final split; consider CLI, discovery/models, Git refresh, sync, diff/rendering, and tests. Keep every resulting Rust file at most 1500 lines, preserve plugin management behavior and coverage, and verify the cumulative file-size and test results for all five refactors.

## Notes

[2026-10-03T11:25:43Z · bob-cli-3s.5] Plugin split implemented. Base c2c54a4b5da85a67555f5f7d085ad84d37630400 clean; src/native/plugins.rs was 2215 lines (1526 pre-tests, 689 tests), no src/native/plugins/ dir. After: plugins.rs facade 17, plugins/cli.rs 314, diff.rs 98, git.rs 171, model.rs 236, render.rs 366, scan.rs 141, sync.rs 258, tests.rs 683 (cargo fmt applied). No plugins/mod.rs. Cumulative audit: all five components under 1500 (capture_complete max 783, capture_task_toggle max 810, task_status_hooks_write max 859, capture_clip max 846, plugins max 683). Dependency flow per plan: cli->{git,scan,sync,render,model}, sync->{model,diff,git,scan}, scan/diff/git->model, render->model. Facade re-exports only run/build_cli; ceiling pub(super) except those two; SyncState/VaultState presentation in render; success_json in render; thresholds in diff; vault_file_is_dirty in git; read_manifest/read_sorted_directory in scan; FileOutcome private in sync; single TEMP_COUNTER in tests.rs; truncate test imports crate::native::style::truncate. Tests preserved with stable paths: 17 unit native::plugins::tests::* and 13 integration plugins::* pass; cargo test plugins adds help/completion::vault::plugins_come_from_the_repo_checkout (16 cli) all pass; cargo test --test cli completion 106 pass. Ran: cargo fmt, cargo test --lib plugins::, cargo test --test cli plugins::, cargo test plugins, cargo test --test cli completion, cargo fmt --check (pass), git diff --check (pass), cargo clippy --all-targets --all-features (pass, pre-existing warnings only), five-component line audit (pass), just all (fmt+clippy pass; full cargo test 1560 pass, 1 fail noted below). PROPOSED FOLLOW-UP: pre-existing BOB_DAY_FILE race in capture_pomodoros::tests::missing_note_and_missing_section_are_warning_successes — failed under default parallel just all (assertion left==1 right==0 at capture_pomodoros.rs:1196), passes in isolation and with --test-threads=4; src/native/capture_pomodoros.rs untouched by this refactor (git diff names only plugins.rs + new plugins/); matches phase bob-cli-3s.3 prior evidence; did not run a clean-base worktree reproduction this turn. No new tests added; no docs/Cargo.toml/Justfile/plugin-source/bob-plugins changes; no bob plugins sync deploy.

[2026-10-03T11:25:50Z · bob-cli-3s.5] Split src/native/plugins.rs (2215) into facade (17) + cli 314, diff 98, git 171, model 236, render 366, scan 141, sync 258, tests 683; all files <=1500, no plugins/mod.rs. Preserved 17 unit + 13 integration plugin tests with stable paths; broader plugins filter and 106 completion tests pass. Cumulative five-component audit pass. cargo fmt --check, clippy, diff --check pass; just all: 1560 pass with 1 pre-existing capture_pomodoros BOB_DAY_FILE parallel flake (passes isolated/threads=4, file untouched).

## Dependencies

- **Depends on:** [bob-cli-3s.4](bob-cli-3s.4.md) ✓ · ⧖ 2026-10-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3s.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-3s.5.md) | [bob-cli-3s.5](bob-cli-3s.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`bfa3ac9`](https://github.com/bobs-org/bob-cli/commit/bfa3ac904d194fc26e92c9c70706f510a552eccd) | refactor(plugins): split plugin management into focused modules | [bob-cli-3s.5](bob-cli-3s.5.md) | 2026-10-03 07:26:42 EDT |
