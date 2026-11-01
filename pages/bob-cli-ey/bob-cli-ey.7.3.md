# Bead: bob-cli-ey.7.3 — Bob Mac Capture macOS test regressions from the directive and drawer phases

[Bead Pages](../README.md) / [bob-cli-ey.7](bob-cli-ey.7.md) / bob-cli-ey.7.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ey.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ey.land.md) · **Assignee:** `bob-cli-ey.7.3` · **Size:** medium
**Created:** 2026-11-01 03:50:53 EST · **Closed:** 2026-11-01 04:47:31 EST
**Plan:** [202611/finish\_capture\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_capture_drawers.md)

## Description

mac-ci-regressions: fix the twelve macOS-hosted XCTest regressions that the mac-directives and mac-drawers phases introduced (explicit completion submit, Open Hint, template shelf, unselected type menu). Leave bob-cli-f3's seven baseline failures alone. Verify with a macOS CI run.

## Notes

[2026-11-01T09:08:47Z · bob-cli-ey.7.3] Root causes (product vs test): (1) Open Hint chip was gated on primaryActionEnabled/grammar, hiding it with no preview yet and with legacy previewResults; product now shows the chip whenever hasDraft and the plan is available, still disabling the button until Capture is enabled. (2) Explicit completion splice of replacement "cash" over "Call @ca" range (6,8) yields "Call @cash"; tests waited for "Call cash". Client-replaced case now uses setProcessClient so the new bob re-parses. (3) Template list first row fieldCount is 1 in capture-templates-list-populated.json. Delete record raced optimistic local removal; wait now includes argv=capture-templates delete. Command-S refusal now expects bob copy "add `%t` to the draft's first item to save it as a template". (4) Unselected type menu Tab uses fixture replacement "#build" (no trailing space); Up selects last of the six fixture rows. portable-check on athena: 1898 tests, 0 failures. just docs-check passed. Mac scratch typecheck skipped (mac SSH timed out). macos-ci-check next.

[2026-11-01T09:32:18Z · bob-cli-ey.7.3--1] CI 41291891532 SHA dfdd52e: 11 of 12 gone. Remaining of the twelve: testExplicitCompletionSubmitIsCanceledWhenBobClientIsReplaced timed out at :525 because setProcessClient left suppressedCompletionAcceptanceDraft set, so editorTextDidChange returned without re-parsing. NEW: testTwoClipboardChangesSupersedeOlderPreviewsForTheSameDraft got second newest (fake-bob dry-run sequence file race; passed on master 41289488292). f3 seven all still failed. Fixes: clear suppression on client replace; lock dry-run sequence increment; waitUntil requires newest lines. portable-check 1898 ok. Re-running macos-ci-check.

[2026-11-01T09:47:16Z · bob-cli-ey.7.3--2] CI 41293639210 SHA 77e056239a792471c597eaa349cd1108a99fae28: all twelve mac-ci-regressions XCTests passed. Failed tests are exactly the bob-cli-f3 seven baseline (testToggleLineCaseUndoRestoresOriginalLine, testTaskTypeRetypeMoveKeepsDraftAndUsesEnsureNextAction, testPlusAfterCaretIDSwitchesToSubBulletInOneUndoStep, testPlusToggleUndoRestoresLiteralPostKeyDraftOnce, testTypedPlusAsWholeItemOpensActiveTaskPickerThroughKeyIntent, testBareLeadingTrailingAndChildMarkersOpenTaskTypeMenu, testTypedRowDoesNotWriteVisibility). No new failures. Prior remaining of the twelve (testExplicitCompletionSubmitIsCanceledWhenBobClientIsReplaced timeout) and the sequence-race clip preview test from 41291891532 are gone. macos-ci-check exit 1 is the allowed f3 baseline. epic-symbols: none.

[2026-11-01T09:47:31Z · bob-cli-ey.7.3--2] CI 41293639210 SHA 77e0562: all twelve mac-ci-regressions XCTests passed. Failed tests are exactly the bob-cli-f3 seven baseline. No new failures. Client-replace cancel and clip-preview sequence-race from 41291891532 are gone.

## Dependencies

- **Blocks:** [bob-cli-ey.7.4](bob-cli-ey.7.4.md) ◐ · ⧖ 2026-11-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ey.7.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ey.7.3.md) | [bob-cli-ey.7.3](bob-cli-ey.7.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@b48d1b4`](https://github.com/bobs-org/bob-mac-capture/commit/b48d1b4dcd8aaf8dacfd1f21517b2708f23e01d7) | fix(mac-capture): restore Open Hint chip and hosted XCTest contracts | [bob-cli-ey.7.3](bob-cli-ey.7.3.md) | 2026-11-01 04:49:20 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ey.7.3--2][1] | Need the phase scope, design file, notes, and DECISIONS before closing | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ey.7.3.md

<!-- sase:referenced-by:end -->
