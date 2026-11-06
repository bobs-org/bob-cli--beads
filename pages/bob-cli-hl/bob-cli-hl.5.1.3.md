# Bead: bob-cli-hl.5.1.3 — Render merge-in bands and capture outcome copy

[Bead Pages](../README.md) / [bob-cli-hl.5.1](bob-cli-hl.5.1.md) / bob-cli-hl.5.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-hl.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hl.5.md) · **Assignee:** `bob-cli-hl.5.1.3` · **Size:** medium
**Created:** 2026-11-06 01:47:45 EST · **Closed:** 2026-11-06 03:04:43 EST
**Plan:** [202611/capture\_merge\_in\_mac.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_merge_in_mac.md)

## Description

band: build CaptureMergeInPresentation and render complete, pending, and refusal states inside the new-task card. Reuse transfer rows and Pull-In controls, preserve Similar tasks, and implement footer, status, notification, and settled accessibility copy.

## Notes

[2026-11-06T08:04:43Z · bob-cli-hl.5.1.3] Band complete: CaptureMergeInPresentation (complete/pending/refusal pure copy) with 9 new tests; complete band in standardPreviewItem reusing Pull-In controls above Similar-tasks; pending card in idle via currentMergeInPending; refusal card with explicit rewrite buttons via mergeInRefusalPresentation; primaryAction Capture & merge N (bulk keeps Capture), live+committed status Would/Created create-and-merge, notification Created+per-source body, settled merge-in VoiceOver announcements. Verified: swift build --build-tests ok, CaptureMergeInPresentationTests 9/9 pass, full swift test 2236 tests 0 failures (1 skipped), swift format lint exit 0. Mac AppKit/SwiftUI typecheck and macOS CI render/hosted coverage unverified on Linux host.

## Dependencies

- **Depends on:** [bob-cli-hl.5.1.2](bob-cli-hl.5.1.2.md) ✓ · ⧖ 2026-11-06
- **Blocks:** [bob-cli-hl.5.1.4](bob-cli-hl.5.1.4.md) ✓ · ⧖ 2026-11-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-hl.5.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hl.5.1.3/README.md) | [bob-cli-hl.5.1.3](bob-cli-hl.5.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@e30a2f4`](https://github.com/bobs-org/bob-mac-capture/commit/e30a2f44437ead3ebedd7b38fb79b1065279dc13) | feat(capture): render merge-in bands and capture outcome copy | [bob-cli-hl.5.1.3](bob-cli-hl.5.1.3.md) | 2026-11-06 03:05:45 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hl.5.1.3][1] | Need the phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hl.5.1.3/README.md

<!-- sase:referenced-by:end -->
