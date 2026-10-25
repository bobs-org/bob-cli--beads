# Bead: bob-cli-an.6.6.6.5.6.4 — Make the three CapturePanelModelTests submit-argv tests pass on macOS CI

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6](bob-cli-an.6.6.6.5.6.md) / bob-cli-an.6.6.6.5.6.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.4` · **Size:** large
**Created:** 2026-10-24 09:36:39 EDT · **Closed:** 2026-10-24 11:31:22 EDT
**Plan:** [202610/backlog\_batch6\_color\_quote\_walk\_blocks\_shift\_promotion\_race\_mac\_panel\_ci.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch6_color_quote_walk_blocks_shift_promotion_race_mac_panel_ci.md)

## Description

mac-panel-argv-ci: resolve bob-cli-be by finding why the bare x*!2 and = override-restart submit argv no longer reach the fake-bob record, then fix the client or fixture without weakening the assertions.

## Notes

[2026-10-24T15:31:07Z · bob-cli-an.6.6.6.5.6.4--5] VERIFIED RESULT (2026-10-24): Root cause on SHA 833e58259f69bb365e13ada87ebd80de83ea23c4 was an expectation mismatch in the new regression test: fake-bob omits the pull_in capability, so decoding correctly yields nil; the test expected Optional(false), causing three assertions to fail for x*, x!, and x*2. The correction changes only those expected values to nil and keeps all strict argv assertions. Expected writes: x*, x!, x*2 each use capture --format json --refuse-override -- <draft>; x*!2 uses capture --format json --require-pull-in-choice --refuse-override -- x*!2; confirmed override = uses capture --format json --require-pull-in-choice -- =; the unpreviewed override first uses --refuse-override and the second Return uses --require-pull-in-choice. `just portable-check` passed (exit 0). On the Mac scratch copy, `./Scripts/bundle.sh --identity -` and `just typecheck-tests` both passed in one set -e command (exit 0); its EXIT cleanup trap removed /tmp/bob-mac-capture-argv-pQtZiugWXv. Local XCTest is unavailable because the Mac has Command Line Tools only; CI supplies runtime test evidence. Exact-SHA macOS 26 SwiftPM CI passed on 97597714441a3394c2b22284cbbc96f1308c561a: https://github.com/bobs-org/bob-mac-capture/actions/runs/40105623623. The Test step passed all three named CapturePanelModelTests; complete BobMacCaptureTests passed 151 tests with 0 failures; the full package passed 2966 tests with 0 failures. Lint, Build, Bundle, plist/signature verification, launch smoke test, and install/reinstall passed; conditional hang-sample and launch-diagnostic uploads were skipped. No change-caused failure remains.

[2026-10-24T15:31:22Z · bob-cli-an.6.6.6.5.6.4--5] Closed after verified portable-check and Mac scratch bundle/typecheck passed, plus green exact-SHA macOS 26 CI on 97597714441a3394c2b22284cbbc96f1308c561a. All three required tests passed; BobMacCaptureTests passed 151/151 and the full suite passed 2966/2966. Closure applies only to this phase.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.4.md) | [bob-cli-an.6.6.6.5.6.4](bob-cli-an.6.6.6.5.6.4.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.4--1][1] | Need the assigned phase scope and existing completion notes before implementing | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.4.md

<!-- sase:referenced-by:end -->
