# Bead: bob-cli-t.4.1 — Restore the macOS test and release pipeline

[Bead Pages](../README.md) / [bob-cli-t.4](bob-cli-t.4.md) / bob-cli-t.4.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-t.land](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.bob-cli-t.land.md) · **Assignee:** `bob-cli-t.4.1` · **Size:** small
**Created:** 2026-08-15 11:31:15 EDT · **Closed:** 2026-08-15 11:35:58 EDT
**Plan:** [202608/land\_multi\_capture.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/land_multi_capture.md)

## Description

restore_macos_test_compilation: resolve bob-cli-x by making pure indentation helpers safely nonisolated so the macOS test target compiles without weakening main-actor protection around AppKit and model mutation.

## Notes

[2026-08-15T15:35:58Z · bob-cli-t.4.1] Implemented bob-cli-x locally in bob-mac-capture at a1ae3fd by marking only CapturePanelController.bulletIndentationEdit, its pure helper chain, and their immutable constants nonisolated; AppKit responder lookup, NSTextView mutation, completion dismissal, and CapturePanelModel calls remain main-actor isolated. Reproduced CI failure from gh run 31892613742 logs as ActorIsolatedCall in the nonisolated bulletIndentationEdit tests. Verified git diff --check passed and swift build --target CaptureCore passed on Linux with existing bob-cli-w Sendable warnings. just format-lint/build/test and full BobMacCapture SwiftPM builds are not locally runnable on this Linux host because no Apple developer tools/macOS SDK/AppKit are available; bob-cli-x remains open with implementation note for exact-head macOS 26 CI proof.

[2026-08-15T15:37:04Z · bob-cli-t.4.1] Verified git diff --check passed; swift build --target CaptureCore passed on Linux with existing warnings; macOS/Xcode-backed just format-lint, build, test and AppKit tests remain unavailable on this Linux host; implementation left responder/model mutation main-actor isolated while making pure indentation resolver nonisolated.

## Dependencies

- **Blocks:** [bob-cli-t.4.3](bob-cli-t.4.3.md) ◐ · ⧖ 2026-08-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-t.4.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-t.4.1/README.md) | [bob-cli-t.4.1](bob-cli-t.4.1.md) | 0 |
