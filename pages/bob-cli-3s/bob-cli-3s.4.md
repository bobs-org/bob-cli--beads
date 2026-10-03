# Bead: bob-cli-3s.4 — Split clipboard capture into focused modules

[Bead Pages](../README.md) / [bob-cli-3s](README.md) / bob-cli-3s.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0vn](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0vn.md) · **Assignee:** `bob-cli-3s.4` · **Size:** large
**Created:** 2026-10-03 05:16:50 EDT · **Closed:** 2026-10-03 07:03:04 EDT
**Plan:** [202610/split\_largest\_rust\_files.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/split_largest_rust_files.md)

## Description

split-capture-clip: After split-task-status-hooks-write, reinspect src/native/capture_clip.rs and plan its final split; consider clipboard providers/history, content planning/rendering, attachment reservations, persistence, and tests. Keep every resulting Rust file at most 1500 lines and preserve platform gates, rollback behavior, and coverage.

## Notes

[2026-10-03T11:02:53Z · bob-cli-3s.4] Split done: src/native/capture_clip.rs (2239 lines) is now a 27-line facade over src/native/capture_clip/: model.rs 130 (ClipMode/AttachmentKind/AttachmentOutput/ClipOutput+file_confirmations, PlannedFile/PlannedFileKind, ClipPlan shell, ClipReservations/FileReservations), clipboard.rs 229 (providers, history override/merge, normalization), clipy.rs 209 (read-only SQLite history, cfg macos-or-test), plan.rs 252 (entry/history planners, list/structure decisions), render.rs 68 (header validation/rendering, inline/lines outputs), files.rs 411 (path/URI classification, attachment/snippet planning, destinations), persist.rs 130 (ClipPlan.save, TEMP_COUNTER, atomic writes, rollback cleanup), tests.rs 846 (all 19 tests, stable native::capture_clip::tests::* paths). No mod.rs root. Deps flow plan->{model,files,render}, files->{model,render}, render/persist->model, clipboard->clipy (macOS). Tests preserved: 19 lib + 15 clip + 11 batch, all passing focused. fmt/clippy clean (zero capture_clip warnings; facade re-exports used internally). First just all fully green. Later full-suite default-parallelism runs flaked only in untouched modules: capture_pomodoros missing_note test (documented pre-existing BOB_DAY_FILE race per bob-cli-3s.3 notes 1/3; passes isolated + 4-thread lib 1561/1561) and ob lock_wait_behavior (Contended; passes isolated). No behavior/contract changes; Linux-run; macOS-only branches cfg-inspected. PROPOSED FOLLOW-UP: track ob lock_wait_behavior intermittent Contended failure under full-suite parallelism (passes isolated + sometimes 4-thread); independent of this refactor. -m

[2026-10-03T11:03:04Z · bob-cli-3s.4] Facade 27 lines + 8 children (229/209/411/130/130/252/68/846), all <=1500. Preserved 19 lib + 15 clip + 11 batch tests; unit paths stable. cargo fmt, clippy (no capture_clip warnings), focused suites green; just all green once, later full runs flaked only in untouched modules (pomodoros BOB_DAY_FILE race per 3s.3 evidence; ob lock timing), both pass isolated. Linux-run; macOS branches cfg-inspected.

## Dependencies

- **Depends on:** [bob-cli-3s.3](bob-cli-3s.3.md) ✓ · ⧖ 2026-10-03
- **Blocks:** [bob-cli-3s.5](bob-cli-3s.5.md) ◐ · ⧖ 2026-10-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3s.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-3s.4.md) | [bob-cli-3s.4](bob-cli-3s.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`c2c54a4`](https://github.com/bobs-org/bob-cli/commit/c2c54a4b5da85a67555f5f7d085ad84d37630400) | refactor(capture-clip): split capture\_clip into focused modules | [bob-cli-3s.4](bob-cli-3s.4.md) | 2026-10-03 07:04:42 EDT |
