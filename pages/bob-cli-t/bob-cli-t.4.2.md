# Bead: bob-cli-t.4.2 — Integrate later-item task-ID assignment with batch capture

[Bead Pages](../README.md) / [bob-cli-t.4](bob-cli-t.4.md) / bob-cli-t.4.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-t.land](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.bob-cli-t.land.md) · **Assignee:** `bob-cli-t.4.2` · **Size:** medium
**Created:** 2026-08-15 11:31:15 EDT · **Closed:** 2026-08-15 11:44:30 EDT
**Plan:** [202608/land\_multi\_capture.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/land_multi_capture.md)

## Description

integrate_batch_task_id_flow: add cross-repository regression coverage for all-task completion and inline block-ID assignment in a later batch item, fixing any loss of global ranges, earlier draft items, or one-process capture semantics.

## Notes

[2026-08-15T15:44:30Z · bob-cli-t.4.2] Verified bob-cli-t.4.2: added bob-cli CLI later-item --all-tasks regression and bob-mac-capture process/model/fake-Bob coverage for global UTF-8 ranges, ID prompt success/cancel/server+transport/stale failures, explicit preview/submit full-draft subprocess contract, and capture failure retention. Ran cargo fmt --check, cargo clippy --all-targets --all-features (exit 0; only existing bob-cli-v warnings), cargo test, focused cargo test capture_complete_all_tasks_uses_global_ranges_in_later_batch_item, manual parse/complete/dry-run smoke, git diff --check in both repos, bash -n Tests/Fixtures/fake-bob, fake-Bob JSON checks, swift build --target CaptureCore, and swift build --target CaptureCoreTests. Linux limitations recorded: swift test hits no such module AppKit; just format-lint requires Xcode 26 Apple developer tools.

[2026-08-15T15:46:22Z · bob-cli-t.4.2] Verified cargo fmt --check, cargo clippy --all-targets --all-features, cargo test, focused Rust regression, manual parse/complete/dry-run smoke, git diff --check in both repos, bash -n Tests/Fixtures/fake-bob, fake-Bob JSON checks, swift build --target CaptureCore, and swift build --target CaptureCoreTests. Full swift test is macOS-only here because AppKit is unavailable on Linux; just format-lint requires Xcode 26 Apple developer tools.

## Dependencies

- **Blocks:** [bob-cli-t.4.3](bob-cli-t.4.3.md) ◐ · ⧖ 2026-08-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-t.4.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-t.4.2/README.md) | [bob-cli-t.4.2](bob-cli-t.4.2.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`3beae5b`](https://github.com/bobs-org/bob-cli/commit/3beae5bf7ee67486d0c721e8beaf92f57847e5d8) | test: cover all-task completion ranges in later batch items | [bob-cli-t.4.2](bob-cli-t.4.2.md) | 2026-08-15 11:47:01 EDT |
| bob-mac-capture | [`bob-mac-capture@49f0037`](https://github.com/bobs-org/bob-mac-capture/commit/49f0037c25038ec44641aab4d6de4229322fab83) | test: cover later batch task ID assignment | [bob-cli-t.4.2](bob-cli-t.4.2.md) | 2026-08-15 11:47:46 EDT |
