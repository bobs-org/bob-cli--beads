# Bead: bob-cli-mn.2 — Mac Capture opens the record list on a bare @album/ draft

[Bead Pages](../README.md) / [bob-cli-mn](README.md) / bob-cli-mn.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1d8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1d8.md) · **Assignee:** `bob-cli-mn.2` · **Size:** small
**Created:** 2026-11-17 06:44:44 EST · **Closed:** 2026-11-17 08:11:39 EST
**Plan:** [202611/album\_slash\_record\_list.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/album_slash_record_list.md)

## Description

mac_record_list: in bob-mac-capture, skip the cached route list when the caret's record_route span is the whole draft so bob's record_target rows show; add real-bob fixtures, fake-bob cases, hosted tests, and docs; verify on macOS CI.

## Notes

[2026-11-17T13:11:39Z · bob-cli-mn.2] cachedRouteCompletion defers a whole-draft record_route with caret at end to capture-complete; fake-bob + generated eat-bare fixtures; hosted tests cover @eat/ record_target vs title-bearing cache; just portable-check, just docs-check, Mac scratch typecheck-tests, and Scripts/macos-ci-check SHA 31542f19 run 44086243927 all passed.

[2026-11-17T13:42:05Z · bob-cli-mn.2--1] Landing SHA 19a23f40 failed macOS CI run 44090592205 on CaptureAliasTipPanelTests.testFilteringKeepsTheShownTipAnchoredToTheSigil: rewrite lost the race to capture-complete, so the list first-frame dropped the tip as late_reply (tipsShown=0). The snapshot SHA 31542f19 tree matched the landing and had passed. Hardening that hosted test with the 200ms debounce plus FAKE_BOB_CAPTURE_COMPLETE_DELAY_SECONDS=0.15 already used by sibling alias-tip tests.

[2026-11-17T14:30:19Z · bob-cli-mn.2--2] Master CI 44102169141 on 991c877e failed Check scripts, not the alias-tip hosted test: GateTests.test_sigterm_during_push got -9 because communicate(timeout=6) SIGKILL'd the gate after the stalled push printed the 5s command-timeout and before cleanup finished. Widening that wait (and SIGINT sibling) to 15s with TOTAL=20 CLEANUP=5. -r Record the Check scripts flake diagnosis on the closed phase bead

[2026-11-17T15:08:55Z · bob-cli-mn.2--3] Record the Test-step alias-tip flake diagnosis on the closed phase bead Master CI 44104221689 on 22a95b64 failed Test (not Check scripts): CaptureAliasTipPanelTests.testChangedSeparatorReplyDoesNotDisableTheNextTipRequest timed out waiting for the follow-up @ list tip. Debounce 0 let capture-complete open the list first and drop the rewrite as late_reply. Giving that hosted test the 200ms debounce plus FAKE_BOB_CAPTURE_COMPLETE_DELAY_SECONDS=0.15 sibling first-frame tests already use. just portable-check passed; Mac scratch typecheck-tests passed (stub). -r

## Dependencies

- **Depends on:** [bob-cli-mn.1](bob-cli-mn.1.md) ✓ · ⧖ 2026-11-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-mn.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-mn.2.md) | [bob-cli-mn.2](bob-cli-mn.2.md) | 4 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@19a23f4`](https://github.com/bobs-org/bob-mac-capture/commit/19a23f40db527d6db0d1992aa24a45d13a5909b0) | feat(capture): list album records after a typed @album/ | [bob-cli-mn.2](bob-cli-mn.2.md) | 2026-11-17 08:13:30 EST |
| bob-mac-capture | [`bob-mac-capture@991c877`](https://github.com/bobs-org/bob-mac-capture/commit/991c877e5cfe3030fb9516dee452af2f20f39f39) | test(capture): keep the alias tip when the route list filters | [bob-cli-mn.2](bob-cli-mn.2.md) | 2026-11-17 09:21:10 EST |
| bob-mac-capture | [`bob-mac-capture@22a95b6`](https://github.com/bobs-org/bob-mac-capture/commit/22a95b6425efd7eb560103d574adc3d7689035ac) | test(ci): wait out SIGTERM cleanup in macos-ci-check tests | [bob-cli-mn.2](bob-cli-mn.2.md) | 2026-11-17 09:32:22 EST |
| bob-mac-capture | [`bob-mac-capture@4d96d4a`](https://github.com/bobs-org/bob-mac-capture/commit/4d96d4a5a9027967c18f0e25618ef064c4c001ff) | test(capture): keep the follow-up tip after a separator rewrite | [bob-cli-mn.2](bob-cli-mn.2.md) | 2026-11-17 10:10:53 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-mn.2--1][1] | Need the phase scope and design file after CI failure | 1 |
| read-by | [agent:bob-cli-mn.2--2][1] | Inspect phase bead after Check scripts CI failure | 1 |
| read-by | [agent:bob-cli-mn.2--3][1] | Need phase scope after macOS Test step failure | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-mn.2.md

<!-- sase:referenced-by:end -->
