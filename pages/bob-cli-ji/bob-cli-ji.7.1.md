# Bead: bob-cli-ji.7.1 — Complete Bob Mac Capture Event note mode

[Bead Pages](../README.md) / [bob-cli-ji.7](bob-cli-ji.7.md) / bob-cli-ji.7.1

**Status:** ✓ closed · **Resolution:** (unrecorded) · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ji.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ji.7.md) · **Assignee:** `bob-cli-ji.7.1.land`
**Created:** 2026-11-10 10:29:45 EST
**Plan:** [202611/mac\_event\_note\_mode.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_event_note_mode.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/mac_event_note_mode.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 4 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_event_note_mode.md

<!-- sase:links:end -->

## Description

Complete bob-cli-ji.7: open a private event note from any capture draft with Command-E, the status menu, or a Calendar row; choose an event and scope; edit with Bob's highlights and a faithful hatched time rail; save, clear, and undo through bob gcal note JSON while preserving capture text and undo history. Ship the documentation and verify the exact Swift tree with macOS CI.

## Notes

[2026-11-10T22:35:06Z · bob-cli-ji.7.1.land] FOLLOW-UP TRIAGE (land agent): (1) CaptureAliasTipPanelTests failures (7.1.2 #1, 7.1.3 #1, 7.1.4 #1-#2, 7.1.5 #2) -> new ci task bob-cli-jx. The three waitUntil-timeout tests fail on every run since aafed83. The intermittent testEditBeforeTheReplyDropsTheTip and testChangedSeparatorReplyDoesNotDisableTheNextTipRequest are folded into its scope. Related to bob-cli-jk and closed epic bob-cli-j9. (2) Mac typecheck-tests @MainActor tearDown/ledgerSuites error (7.1.5 #1) -> new ci task bob-cli-jy (from bob-cli-j9's 542a37d). (3) Clean-base docs word budgets (7.1.1 #1, 7.1.6 #1): +1 on bob-cli-h9 for protocol.md, and new ci task bob-cli-jz for capture-panel, capture-previews, keyboard, and plugins bob-navigation-hotkeys. json-outputs is no longer over after 891fa3e4. The epic's own growth of keyboard.md (+32 words) and protocol.md (+68) is epic work and goes to the remaining-work tale. (4) Redundant try at EventTimeRailDesignTests.swift:32 (7.1.3 #2): declined as a follow-up. The epic caused it, so the remaining-work tale fixes it. (5) Discovered during landing: CaptureSeparatorToggleTests.testOlderBobMoveAliasReplyLeavesLiteralWithoutOpeningPicker flaked on docs-only master 1498f34 (run 42912210207). Same fixed-200ms-sleep root cause as bob-cli-jc, so I added a +1 there.

[2026-11-11T02:59:22Z · bob-cli-ji.7.1.land--8] VERIFICATION: Bob just check passed before Mac-only layout work; Athena portable-check passed 2,468 tests (1 skipped). Exact-SHA macOS Actions run 42947559531 at c90a69df63207a130c17c7ff62a2287455a734ac passed Swift formatting and Build; the saved-note editor test passed. Only three CaptureAliasTipPanelTests failures remained, tracked by bob-cli-jx. Reviewed all 26 event-note and 52 event-rail render fixtures, including the 480x520 light/dark panels; footer controls remain visible while content scrolls.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ji.7.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ji.7.1.land.md) | [bob-cli-ji.7.1](bob-cli-ji.7.1.md) | 6 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4c1f7dd`](https://github.com/bobs-org/bob-cli/commit/4c1f7dde9f6e8515f069ccfd3e58c30047d76a0e) | fix(gcal): clean event note lint and add preview fixtures | [bob-cli-ji.7.1](bob-cli-ji.7.1.md) | 2026-11-10 18:28:36 EST |
| bob-mac-capture | [`bob-mac-capture@f1e5c99`](https://github.com/bobs-org/bob-mac-capture/commit/f1e5c99c05539d54e71789f8afba95837b8fccc2) | feat(capture): complete event note editing and preview | [bob-cli-ji.7.1](bob-cli-ji.7.1.md) | 2026-11-10 18:29:07 EST |
| bob-cli | [`85e618d`](https://github.com/bobs-org/bob-cli/commit/85e618d889ab2172c29ab5b25cae66d209968936) | test(cli): align catalog and gcal doctor expectations | [bob-cli-ji.7.1](bob-cli-ji.7.1.md) | 2026-11-10 20:14:17 EST |
| bob-mac-capture | [`bob-mac-capture@15e34ba`](https://github.com/bobs-org/bob-mac-capture/commit/15e34bafc9638dc63117ab527719dd327c57085a) | test(capture): check event note footer accessibility bounds | [bob-cli-ji.7.1](bob-cli-ji.7.1.md) | 2026-11-10 20:14:46 EST |
| bob-mac-capture | [`bob-mac-capture@e638795`](https://github.com/bobs-org/bob-mac-capture/commit/e63879582888becb02c51430c012f0c4b6b26592) | test(gcal-note): verify compact editor footer layout | [bob-cli-ji.7.1](bob-cli-ji.7.1.md) | 2026-11-10 22:03:42 EST |
| bob-cli--plans | [`bob-cli--plans@b03a50d`](https://github.com/bobs-org/bob-cli--plans/commit/b03a50db376878c4df63ec373f72d8624a2f4654) | docs(gcal-note): mark Mac event note plan done | [bob-cli-ji.7.1](bob-cli-ji.7.1.md) | 2026-11-10 22:04:14 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ji.7.1.5--1][1] | Need epic DECISIONS before changing editor tests and session | 1 |
| read-by | [agent:bob-cli-ji.7.1.6][2] | Need child epic scope and decisions | 1 |
| read-by | [agent:bob-cli-ji.7.1.land--1][3] | Verify approved epic and parent phase deliverables before closeout | 1 |
| read-by | [agent:bob-cli-ji.7.1.land--5][3] | Inspect child epic status, scope, and blockers before verification closeout | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ji.7.1.5.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ji.7.1.6/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ji.7.1.land.md

<!-- sase:referenced-by:end -->
