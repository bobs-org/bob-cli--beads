# Bead: bob-cli-an.6.6.6.5.6.5.5.2 — Make the Highlights save-scan panel preparation XCTest pass on macOS CI

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5](bob-cli-an.6.6.6.5.6.5.5.md) / bob-cli-an.6.6.6.5.6.5.5.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.2` · **Size:** medium
**Created:** 2026-10-25 07:49:26 EDT · **Closed:** 2026-10-25 08:04:59 EDT
**Plan:** [202610/backlog\_batch8\_listen\_manifest\_mac\_ci\_flakes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch8_listen_manifest_mac_ci_flakes.md)

## Description

mac-save-scan-test: resolve bob-cli-bv by finding why the held-receipt PDF update surface yields no footer clauses at RefsPanelModelTests.swift:2312 and fixing code or fixture without weakening the assertion.

## Notes

[2026-10-25T12:04:49Z · bob-cli-an.6.6.6.5.6.5.5.2] Root cause: footerClauses(for:) in Sources/RefsCore/RefsPDFUpdates.swift never yields a clause for coordination_timeout (busy) holds — only refreshedOpen notes and reading/changed holds. The test fixture at RefsPanelModelTests.swift:2286 built a busy-only receipt, so pdfUpdateFooterClauses was [] by design and XCTAssertFalse(isEmpty) failed. This predates the test: identical code since 9fb67f3, test unchanged since 72cd721, and the banner-only busy contract is documented in docs/refs.md:408 and encoded by passing tests testPDFUpdateSurfaceSetsFooterClausesAndBusyBanner and RefsPDFUpdatesTests.testSurfaceHidesNotificationsWhenVisibleOrDisabledAndDedupesBusyHolds. Fix is fixture-side (production code and docs contract are correct): added a savedFirst refreshed note (ref/papers/open.md) to the receipt, realistic for a Highlights save that refreshed one open PDF while another stayed busy. Assertions unchanged in strength. Evidence: just portable-check exit=0 (1648 tests, 0 failures, Linux Swift 6.0.3); mac scratch copy bundle.sh exit=0 and just typecheck-tests exit=0 (all test targets PASS incl. BobMacCaptureTests), scratch removed. Limitation: mac has Command Line Tools without XCTest so CI must execute the test; watch macOS CI on the landed SHA containing bob-mac-capture Tests/RefsPanelModelTests.swift with the saved-note fixture.

[2026-10-25T12:04:59Z · bob-cli-an.6.6.6.5.6.5.5.2] Fixture fix in bob-mac-capture Tests/RefsPanelModelTests.swift (busy-only receipt gained a savedFirst refreshed note so the surface yields a footer clause; assertions unchanged). Verified: just portable-check exit=0 (1648 tests, 0 failures); mac scratch bundle.sh and just typecheck-tests exit=0 with all test targets PASS; scratch removed. Change left uncommitted for the lander; macOS CI must execute the test on the landed SHA.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.2/README.md) | [bob-cli-an.6.6.6.5.6.5.5.2](bob-cli-an.6.6.6.5.6.5.5.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@2b20d89`](https://github.com/bobs-org/bob-mac-capture/commit/2b20d89ec7a8a6debf6bd8b71681ee623c5d5862) | fix(refs): give Highlights save-scan test a receipt that yields footer clauses | [bob-cli-an.6.6.6.5.6.5.5.2](bob-cli-an.6.6.6.5.6.5.5.2.md) | 2026-10-25 08:06:31 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.2][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.land.md

<!-- sase:referenced-by:end -->
