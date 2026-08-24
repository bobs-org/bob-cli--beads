# Bead: bob-cli-13.3 — Mac capture panel absorbs @@ as you type

[Bead Pages](../README.md) / [bob-cli-13](README.md) / bob-cli-13.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0cv](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.0cv.md) · **Assignee:** `bob-cli-13.3` · **Size:** medium
**Created:** 2026-08-24 15:01:18 EDT · **Closed:** 2026-08-24 16:01:19 EDT
**Plan:** [202608/capture\_global\_destination\_anywhere.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/capture_global_destination_anywhere.md)

## Description

macapp: wire the bob-mac-capture panel to `bob capture-rewrite` so typing a bare `@@` rewrites the draft in place with an announced summary, plus CaptureCore models, process-client lane, tests, and README updates.

## Notes

[2026-08-24T20:01:19Z · bob-cli-13.3] Implemented bob-mac-capture integration with bob capture-rewrite models, process lane, panel trigger/apply flow, fake-bob coverage, tests, and README updates; verified swift build --target CaptureCore, swift build --target CaptureCoreTests, git diff --check, and confirmed swift test --filter CaptureCoreTests is blocked on Linux by AppKit target compilation.

## Dependencies

- **Depends on:** [bob-cli-13.2](bob-cli-13.2.md) ✓ · ⧖ 2026-08-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-13.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-13.3/README.md) | [bob-cli-13.3](bob-cli-13.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@0a31975`](https://github.com/bobs-org/bob-mac-capture/commit/0a3197564f83cfe8cbdeca25afefac64251e571e) | feat(capture): wire mac panel capture rewrite | [bob-cli-13.3](bob-cli-13.3.md) | 2026-08-24 16:02:15 EDT |
