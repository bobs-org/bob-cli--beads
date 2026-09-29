# Bead: bob-cli-2k.1 — Numbered Task Links and outcome selection in the pure close planner

[Bead Pages](../README.md) / [bob-cli-2k](README.md) / bob-cli-2k.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.34](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.34.md) · **Assignee:** `bob-cli-2k.1` · **Size:** medium
**Created:** 2026-09-29 13:45:03 EDT · **Closed:** 2026-09-29 14:06:12 EDT
**Plan:** [202609/close\_task\_selection.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/close_task_selection.md)

## Description

selection-planner: in `src/native/capture_pomodoro_close/`, number the running
session's Task Links. Apply a `CloseSelection` by rewriting only the `#`/`![[…]]`
markers of the numbered lines, then run the unchanged close. Validate numbers
against the lineup, warn when a listed task cannot change status, and expose the
numbered lineup plus a per-row `index`. Every caller passes `None` for now. Pinned
by unit tests on the worked example.

## Notes

[2026-09-29T18:05:59Z · bob-cli-2k.1] PROPOSED FOLLOW-UP: Fix pre-existing clippy deny failure in tests/cli/capture/pomodoro_name.rs:808 (overly_complex_bool_expr with || true); file untouched by this phase, `cargo clippy --all-targets --all-features` fails identically on clean base

[2026-09-29T18:06:12Z · bob-cli-2k.1] selection-planner done: new selection.rs (CloseSelection, numbering, outcome table, OutOfRange/ConflictingDuplicate Display, CRLF-safe rewrite), plan_pomodoro_close takes Option<&CloseSelection> with task_links/index/listed warnings, 3 callers pass None. Verified: cargo test exit 0 (1163 lib incl 45 close tests, 521 cli, all suites ok), cargo fmt clean, clippy clean in touched files. Note: plan x2/x0 blocks collapse orphan notes onto entry line but hand-edits + current binary leave them as deeper bullets; implemented marker-edits + unchanged close (tests assert actual). Pre-existing clippy deny in untouched pomodoro_name.rs recorded as follow-up.

## Dependencies

- **Blocks:** [bob-cli-2k.3](bob-cli-2k.3.md) ✓ · ⧖ 2026-09-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2k.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2k.1/README.md) | [bob-cli-2k.1](bob-cli-2k.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`6f45d38`](https://github.com/bobs-org/bob-cli/commit/6f45d389110426f7e1a52f7e4d2107b0edf99c61) | feat(close): numbered Task Links and outcome selection in pure close planner | [bob-cli-2k.1](bob-cli-2k.1.md) | 2026-09-29 14:07:53 EDT |
