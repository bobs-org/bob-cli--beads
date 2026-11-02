# Bead: bob-cli-fn.4 — Bob Mac Capture presentation

[Bead Pages](../README.md) / [bob-cli-fn](README.md) / bob-cli-fn.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.c1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.c1.md) · **Assignee:** `bob-cli-fn.4` · **Size:** medium
**Created:** 2026-11-01 23:41:35 EST · **Closed:** 2026-11-02 04:42:46 EST
**Plan:** [202611/capture\_route\_lists.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_route_lists.md)

## Description

mac-lists: in bob-mac-capture, apply Bob's block-ID splice on accept, caption the owner task, group list results in the preview, open the first bullet after a lone header, and regenerate fixtures from a real bob.

## Notes

[2026-11-02T09:42:20Z · bob-cli-fn.4] PROPOSED FOLLOW-UP: Verify the AppKit and SwiftUI changes on macOS CI and a real Mac — this host could not compile Sources/BobMacCapture or Tests/BobMacCaptureTests (the Mac was offline, athena has only the Linux toolchain). They were syntax-parsed with swiftc -parse and linted only; CaptureCore (2001 tests) passed on athena. Check CaptureListPanelTests, the owner header in CapturePickerView, the list capsule in CapturePanelView, and Shift-Return after a lone header.

[2026-11-02T09:42:25Z · bob-cli-fn.4] PROPOSED FOLLOW-UP: Picker accepts, including the new block-ID splice, replace the draft through setPlainDraft, which registers no native NSTextView undo step. The phase text asks that Undo restore the pre-accept draft; confirm that on a real Mac and, if it does not, add a controller bridge that applies the accept as one native undoable edit once focus returns to the editor.

[2026-11-02T09:42:30Z · bob-cli-fn.4] PROPOSED FOLLOW-UP: After the Mac Capture docs land, add a Capture lists bullet (docs/capture-lists.md, registered in bob-mac-capture docs/nav.yml) under Capture in bob-cli docs/reference/mac-capture/index.md. It was left out so bob-cli CI cannot link a page that is not on the Mac repo master yet.

[2026-11-02T09:42:46Z · bob-cli-fn.4] Mac-lists presentation implemented in bob-mac-capture. Verified on athena (Linux Swift 6.0.3): swift build --build-tests and swift test, 2001 tests, 0 failures, including the new CaptureListTests (splice apply for same-line, nested, owner-ID replace, caret sigil, project-note and type-through cases; owner caption; list capsule grouping; lone-header newline). Fixtures regenerated from a real bob built at bob-cli 35c46693 via Scripts/generate-list-fixtures.sh, whose self-checks pass. just docs-check, just check-scripts pass. NOT verified: Sources/BobMacCapture and Tests/BobMacCaptureTests (incl. CaptureListPanelTests) were only syntax-parsed and linted, since the Mac was offline and the Linux toolchain has no AppKit; macOS CI has not run on this change. CaptureGrammarGate.minimumRevision stays 3. Follow-ups recorded as PROPOSED FOLLOW-UP notes.

## Dependencies

- **Depends on:** [bob-cli-fn.3](bob-cli-fn.3.md) ✓ · ⧖ 2026-11-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-fn.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fn.4/README.md) | [bob-cli-fn.4](bob-cli-fn.4.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-fn.4][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fn.4/README.md

<!-- sase:referenced-by:end -->
