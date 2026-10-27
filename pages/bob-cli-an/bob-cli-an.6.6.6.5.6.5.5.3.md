# Bead: bob-cli-an.6.6.6.5.6.5.5.3 — Make the inbox route-card confirm argv XCTest pass on macOS CI

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5](bob-cli-an.6.6.6.5.6.5.5.md) / bob-cli-an.6.6.6.5.6.5.5.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.3` · **Size:** medium
**Created:** 2026-10-25 07:49:26 EDT · **Closed:** 2026-10-25 08:06:42 EDT
**Plan:** [202610/backlog\_batch8\_listen\_manifest\_mac\_ci\_flakes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch8_listen_manifest_mac_ci_flakes.md)

## Description

mac-inbox-route-argv: resolve bob-cli-bw by reconciling the route-card confirm argv with the bob capture inbox-route contract at CaptureInboxRouteChoiceModelTests.swift:32.

## Notes

[2026-10-25T12:06:35Z · bob-cli-an.6.6.6.5.6.5.5.3] Baseline: CaptureInboxRouteChoiceModelTests.testPreviewOpensRouteCardAndReturnSubmitsOpaqueAnswer passes line 31 (captureCallCount==2) but fails line 32 exact argv match. Preview fixture inbox-route-preview-one.json reports pull_in.supported=true with offer_count=0, so dispatchCapture sent --require-pull-in-choice ahead of --require-inbox-route-choice, breaking the expected contiguous substring.

Fix: Sources/BobMacCapture/CapturePanelModel.swift dispatchCapture now uses requirePullInChoice: selection == nil && inboxRouteAnswers == nil, so pure inbox-route confirms send only --inbox-route, --require-inbox-route-choice, --refuse-override as the test and docs/capture.md require. Combined pull-in+route submits already have selection!=nil so unchanged; normal submits (answers==nil) unchanged.

Tests: just portable-check exit 0 (1648 tests pass); mac scratch rsync (excl .build/.git) bundle.sh Build complete + just typecheck-tests PASS BobMacCaptureTests/InstallHelper/CaptureCore/RefsCore, scratch removed. XCTest not executed locally (mac has CLT without XCTest); CI runs tests.

Watch: bob-mac-capture base 569cb36 plus this one-line fix; lander should monitor macOS CI on landed SHA for the two 3087-test failures.

[2026-10-25T12:06:42Z · bob-cli-an.6.6.6.5.6.5.5.3] Fixed inbox-route confirm to omit --require-pull-in-choice when inbox answers present; portable-check 1648 pass and mac bundle+typecheck-tests PASS, scratch removed; XCTest left for macOS CI on landed SHA

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.3][1] | Need full phase scope including DECISIONS | 2 |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.land.md

<!-- sase:referenced-by:end -->
