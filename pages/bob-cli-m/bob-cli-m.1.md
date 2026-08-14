# Bead: bob-cli-m.1 — Line-aware capture grammar and Markdown output

[Bead Pages](../README.md) / [bob-cli-m](README.md) / bob-cli-m.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.00w.f0.f0.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.00w.f0.f0.w0.md) · **Assignee:** `bob-cli-m.1` · **Size:** medium
**Created:** 2026-08-14 10:54:44 EDT · **Closed:** 2026-08-14 11:27:59 EDT
**Plan:** [202608/capture\_authored\_sub\_bullets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/capture_authored_sub_bullets.md)

## Description

line-aware-capture: make bob-cli own a line-preserving capture model, line-terminal marker extraction, authored-child rendering, compatible JSON and stdin contracts, documentation, and exhaustive Rust coverage across every capture mode.

## Notes

[2026-08-14T15:27:43Z · bob-cli-m.1] PROPOSED FOLLOW-UP: tests/cli.rs nightly_runs_shared_sync_once_then_wrapped_steps_in_order is flaky under full-suite parallel `cargo test` (observed intermittent "Text file busy (os error 26)" from the `ob sync` shim); passes reliably in isolation. Unrelated to the line-aware-capture change — likely a parallel-test binary-recompile race. Worth investigating serialization/locking for that test.

[2026-08-14T15:27:59Z · bob-cli-m.1] Implemented the line-aware capture model per the epic plan: capture_language.rs now splits TEXT into physical lines (LF/CRLF/bare-CR), the first line is the parent and later flat -/*/+ lines become authored children, with capture-wide s:<N>/p:<N>/%.../@route markers recognized in the terminal region of ANY line (leading-route form preserved only on line 1) and cross-line duplicates rejected before any write. Added ParsedCaptureText.sub_bullets and EditorParse.sub_bullets, new diagnostics (invalid_child_line, empty_child_after_markers, duplicate_capture_marker), and made capture-complete's cursor-aware completion scope to the physical line under the cursor. capture.rs renders authored children at the target's dominant indentation in block order parent/authored-children/clip-children/schedule-log, adds JSON+human sub_bullets output, and (with capture-parse/capture-complete) now reads the complete piped stdin stream instead of one line. Updated README.md and all three commands' --help text. Verified: cargo test capture_language (76 unit tests), cargo test --test cli capture (122 integration tests), full cargo test (525 unit + 304 CLI + 27+31+1 other = all green), just all (fmt+lint+test), just install-smoke, git diff --check, and manual end-to-end smoke test of bob capture/capture-parse/capture-complete against a real temp vault. Backward compatibility confirmed: every pre-existing test passed unchanged (only 2 tests needed updates for intentional stdin/behavior changes documented in the plan).

[2026-08-14T15:28:50Z · bob-cli-m.1] Line-aware capture model verified: 525 unit tests + 304 CLI integration tests pass, just all, just install-smoke, git diff --check, and manual end-to-end smoke test all succeeded.

## Dependencies

- **Blocks:** [bob-cli-m.2](bob-cli-m.2.md) ◐ · ⧖ 2026-08-14

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-m.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-m.1/README.md) | [bob-cli-m.1](bob-cli-m.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`2d6b0af`](https://github.com/bobs-org/bob-cli/commit/2d6b0afe9053ce9ce6ccc6ccb08f73d7948286d0) | feat(capture): make capture text physical-line-aware | [bob-cli-m.1](bob-cli-m.1.md) | 2026-08-14 11:29:18 EDT |
