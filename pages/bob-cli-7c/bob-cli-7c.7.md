# Bead: bob-cli-7c.7 — Bob Mac Capture in-panel pull-in choice step

[Bead Pages](../README.md) / [bob-cli-7c](README.md) / bob-cli-7c.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.11.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.11.linker.w0.md) · **Assignee:** `bob-cli-7c.7` · **Size:** large
**Created:** 2026-10-13 09:48:12 EDT · **Closed:** 2026-10-13 16:56:48 EDT
**Plan:** [202610/successor\_offers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/successor_offers.md)

## Description

mac_choice: decode offer/pull_in fields, number offer rows on the preview cards, add a keyboard multi-select choice step on Return, pass --pull-in on submit, use the --require-pull-in-choice race guard, fix missing copy, and verify on macOS CI.

## Notes

[2026-10-13T19:41:23Z · bob-cli-7c.7--6] Verification evidence for mac_choice (not closed yet; GitHub CI on the published commit is still outstanding).

Implemented in linked bob-mac-capture: decode offer/pull_in contract fields; in-panel successor choice on Return; confirm passes opaque keys via --pull-in; Shift-Return sends none; Esc restores the unchanged draft; --require-pull-in-choice race guard with one write-free clap-unknown retry; README/key/copy updates; fake-bob fixtures and focused tests.

Portable-check: green. Monitor 0aynq1d58b1c, exit 0, ~66s. Refreshed athena scratch /tmp/bmc-successor-choice.7zsUiQ from this working tree, then `just portable-check`. Tool run 43f579748f5fd3cd50c426f6048fe2af.

Local macOS scratch on host mac: app product compiled. Monitor bfg74j4geae9. `./Scripts/bundle.sh --identity -` then `./Scripts/xcode-swift.sh build --build-tests`. Log line: "Build of product 'BobMacCapture' complete! (35.91s)". Test-target build failed with `error: no such module 'XCTest'` starting at Tests/CaptureCoreTests/ActiveTaskPickerPresentationTests.swift:1. Earlier authored Color.tertiary compile error in CapturePanelView.swift was fixed before this rerun. Clean-HEAD scratch /tmp/bmc-successor-choice-clean-head reproduced the same XCTest import failure while compiling the app. Isolated scratches /tmp/bmc-successor-choice.20261013.1918 and /tmp/bmc-successor-choice-clean-head were deleted after that comparison. Installed app/checkouts were not touched.

GitHub Actions CI (formatting, Build, Test, Bundle, signature, launch, install) has not yet run on the commit that will publish this tree; that remains the close gate.

[2026-10-13T19:41:41Z · bob-cli-7c.7--6] PROPOSED FOLLOW-UP: host mac Swift toolchain cannot import XCTest — Isolated scratch ./Scripts/xcode-swift.sh build --build-tests fails with no such module XCTest on Tests/CaptureCoreTests/ActiveTaskPickerPresentationTests.swift:1 after BobMacCapture compiled. Reproduced on clean HEAD at 2837025 in /tmp/bmc-successor-choice-clean-head with the same toolchain/command (monitor bfg74j4geae9). Out of scope for this phase; GitHub macos-26 CI remains the test-runner authority. Do not treat this host failure as an authored regression.

[2026-10-13T20:56:42Z · 7f--2] PROPOSED FOLLOW-UP: RefsInspectorScrollTests fail deterministically on macOS CI since 2837025 — testHostedNotesAtBottomRevealPages (line 632: "inspector offset did not change as expected; lookup=found clip=(0.0, 0.0, 405.0, 462.0) docHeight=239.0 flipped=true insets=NSEdgeInsets(top: 0.0, left: 0.0, bottom: 0.0, right: 0.0)"; line 392: ("6") is not equal to ("8"); line 396: ("1") is not equal to ("2")) and testHostedShortContentRevealsWithNoOffsetChange (line 422: ("3") is not equal to ("6")); reproduced on runs 38438769006, 38462257320, and 38464978866; introduced by plan:202610/refs_inspector_notes_paging.md, which has no bead; masks the Bundle, signature, launch, and install gates for every later commit.

[2026-10-13T20:56:48Z · 7f--2] mac_choice CI close evidence.

Fix commits on bob-mac-capture master:
- b0e2ff277d3de360232499b092b11ed1dfbd6a75 test(capture): fix pull-in choice keyEvent optional String compile error
- 6c4209b7addd06278f43eca2eeb66354f9e62edc test(capture): align pull-in tests with grouped navigation and require-pull-in-choice argv

Final CI run (SHA 6c4209b): https://github.com/bobs-org/bob-mac-capture/actions/runs/38464978866
- Lint Swift formatting: green
- Build: green (both test targets compiled; 2066 tests executed)
- Test: red — 4 failures in 2066 tests, all in RefsInspectorScrollTests
- Bundle, Verify plist and signature, Launch smoke test, and install: skipped after Test, so those four gates stay unverified

Pull-in suites that compiled and passed on that run: CapturePullInChoiceTests, CapturePullInChoiceModelTests, CapturePullInChoiceDesignTests, CapturePullInClientTests, CapturePullInDecodingTests, CaptureSuccessorPresentationTests, NotificationServiceTests, CapturePanelModelTests.

Remaining failures (pre-existing, not 395c521): RefsInspectorScrollTests testHostedNotesAtBottomRevealPages (lines 632/392/396) and testHostedShortContentRevealsWithNoOffsetChange (line 422). Same two tests as 2837025 run 38438769006. Recorded as a PROPOSED FOLLOW-UP note on this bead. Did not edit refs-inspector code or tests. No unrelated flake failures on this run, so no gh run rerun.

Prior CI 38462257320 (SHA b0e2ff2) compiled both targets then failed 31 tests; the 6c4209b test alignment cleared every 395c521-owned failure.

Local checks (from the 6c4209b publish turn):
- Athena scratch /tmp/bmc-mac-choice-ci.JHEWCX: just portable-check passed (1123 tests, 0 failures); scratch deleted.
- Mac scratch /tmp/bmc-mac-choice-ci.21P0cr: ./Scripts/bundle.sh --identity - succeeded (Build of product 'BobMacCapture' complete! (121.11s)). ./Scripts/xcode-swift.sh build --build-tests failed only with error: no such module 'XCTest' (expected; bead note #2). Scratch deleted. Installed app/checkouts were not touched.

bob-mac-capture master is clean and not ahead of origin/master at 6c4209b.

## Dependencies

- **Depends on:** [bob-cli-7c.3](bob-cli-7c.3.md) ✓ · ⧖ 2026-10-13
- **Blocks:** [bob-cli-7c.8](bob-cli-7c.8.md) ✓ · ⧖ 2026-10-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-7c.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-7c.7.md) | [bob-cli-7c.7](bob-cli-7c.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@395c521`](https://github.com/bobs-org/bob-mac-capture/commit/395c5217523aaf28e81f38c8ef5d471d0e9725e7) | feat(capture): add in-panel successor pull-in choice | [bob-cli-7c.7](bob-cli-7c.7.md) | 2026-10-13 15:43:32 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:7f--1][1] | Need current bead notes and close criteria before classifying CI failures | 1 |
| read-by | [agent:bob-cli-7c.7--6][2] | Confirm note text after shell expansion on the proposed follow-up | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.7f.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-7c.7.md

<!-- sase:referenced-by:end -->
