# Bead: bob-cli-29.4 — Editor contract, help, and docs for =x

[Bead Pages](../README.md) / [bob-cli-29](README.md) / bob-cli-29.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.2i](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.2i.md) · **Assignee:** `bob-cli-29.4` · **Size:** medium
**Created:** 2026-09-28 06:24:49 EDT · **Closed:** 2026-09-28 08:29:18 EDT
**Plan:** [202609/capture\_pomodoro\_close.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/capture_pomodoro_close.md)

## Description

close-editor-contract: add the capture-parse `pomodoro_close` mode, span, spec, incomplete state, and `invalid_pomodoro_close` diagnostics. Make capture-complete and capture-rewrite ignore the close suffix. Update the help for capture, capture-parse, and capture-complete, and update docs/capture.md, the task-status-hooks note, and the README.

## Notes

[2026-09-28T12:29:18Z · bob-cli-29.4] Editor contract for =x done: capture-parse pomodoro_close mode/span/spec, incomplete =, invalid_pomodoro_close diagnostics with precise ranges; capture-complete empty success inside =x; capture-rewrite never rewrites =x; help for capture/parse/complete; docs/capture.md Closing section + grammar/kind/span/diagnostic updates; task-status-hooks ownership note; README rows/examples. Verified: cargo fmt --check clean, cargo clippy clean (no new warnings), cargo test all green (967 lib + 495 cli integration). sase bead epic-symbols clean.

## Dependencies

- **Depends on:** [bob-cli-29.3](bob-cli-29.3.md) ✓ · ⧖ 2026-09-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-29.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-29.4/README.md) | [bob-cli-29.4](bob-cli-29.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`24ba977`](https://github.com/bobs-org/bob-cli/commit/24ba977d2d1198019e2af3543e6375ae2357cba2) | feat(capture): expose and document Pomodoro close editor contract | [bob-cli-29.4](bob-cli-29.4.md) | 2026-09-28 08:30:54 EDT |
