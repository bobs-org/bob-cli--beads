# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.4 — Turn bob-mac-capture master CI green on the queued code-key XCTest

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.4` · **Size:** large
**Created:** 2026-10-26 15:53:09 EDT · **Closed:** 2026-10-26 16:28:27 EDT
**Plan:** [202610/backlog\_batch15\_vault\_safety\_pdf\_moves\_and\_red\_gates.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch15_vault_safety_pdf_moves_and_red_gates.md)

## Description

mac-code-key-ci: resolve bob-cli-cr by deciding whether the queued-Return code picker regressed or its expectation is outdated, and fixing that side without weakening assertions.

## Notes

[2026-10-26T20:02:33Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.4] ROOT CAUSE BEFORE EDITS: bob-mac-capture is clean at 591e4fe. The approved plan:202610/ref_code_block_copy.md Initial selection contract explicitly says without a page select block 1. RefsCodePicker.initialSelection (Sources/RefsCore/RefsCode.swift) returns index 0 for nil page, with an existing portable test for that rule; c7a5f37 did not change it. That same commit introduced both testQueuedCodeKeyCopiesWhenCatalogReturns, which opens the ordinary library card without a Highlights Tabs page, and refs-code.json, whose block 1 is makefile/build (3 lines) and block 2 is yaml/refresh (14 lines, page 7). RefsCopyCard.codeLoaded resolves the pending picker and replays queued Return against its initial selection. Therefore the reported makefile copy is the approved behavior and the YAML expectation is incorrect for this setup. Plan a bounded test correction retaining exact payload/HUD assertions, with an explicit page-7 case to retain YAML coverage; no production policy or fixture-order change is justified. Phase had no earlier work notes; epic-symbols currently reports no entries. Implementation and phase closure will follow the required plan handoff; bob-cli-cr remains for the epic lander to close after landed-SHA macOS CI.

[2026-10-26T20:17:11Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.4] IMPLEMENTATION (pre just check): bob-mac-capture still at 591e4fe before the test edit; working tree now dirty only in Tests/BobMacCaptureTests/RefsPanelModelTests.swift. Reconfirmed RefsCodePicker.initialSelection still returns index 0 for nil page; fixture block 1 is makefile (3 lines, page 2) and block 2 is yaml (14 lines, page 7). Replaced testQueuedCodeKeyCopiesWhenCatalogReturns with testQueuedCodeKeyCopiesFirstBlockWhenCatalogReturnsWithoutPage: asserts open card highlightedPage is nil, C enters .codePicker pending, Return before the 80 ms catalog response, exact makefile payload with literal tabs and no added final newline, Copied makefile · 3 lines, one pasteboard write, one completion, card closed. Added testQueuedCodeKeyCopiesPageBlockWhenCatalogReturnsFromHighlightsTab: FakeTabsReader + tabsSnapshot page 7 + prepareForPresentation(source: .highlightsTabs) + wait for .loaded, frozen page 7, queued C/Return while loading, exact 14-line YAML payload, Copied yaml · 14 lines, one write, one completion, card closed. Fixture and production Swift unchanged. just portable-check passed (1672 tests, 0 failures). Mac scratch at /tmp/bob-mac-capture-queued-code-return-expectations: rsync excluding .build/.git, ./Scripts/bundle.sh then just typecheck-tests both passed (PASS BobMacCaptureTests, BobMacCaptureInstallHelperTests, CaptureCoreTests, RefsCoreTests; stub typecheck only), then that scratch copy was removed. epic-symbols: no entries. bob-cli-cr remains for the parent lander after landed-SHA macOS CI. Next: parent-epic just check in the primary bob-cli checkout.

[2026-10-26T20:28:27Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.4--1] Queued-Return XCTest repair verified; this phase is done. bob-cli-cr stays open for the parent lander.

Test correction (bob-mac-capture Tests/BobMacCaptureTests/RefsPanelModelTests.swift only; production Swift, refs-code.json, docs, changelog, versions, and memory untouched):
- Renamed/corrected no-page queued-Return case to testQueuedCodeKeyCopiesFirstBlockWhenCatalogReturnsWithoutPage: nil highlightedPage, C -> .codePicker pending, Return before 80ms catalog, exact makefile payload with literal tabs and no added final newline, Copied makefile · 3 lines, one pasteboard write, one completion, card closed.
- Added testQueuedCodeKeyCopiesPageBlockWhenCatalogReturnsFromHighlightsTab: FakeTabsReader, tabsSnapshot page 7, prepareForPresentation(source: .highlightsTabs), wait for .loaded, frozen page 7, queued C/Return while loading, exact 14-line YAML payload, Copied yaml · 14 lines, one write, one completion, card closed.

Local validation:
- just portable-check in bob-mac-capture: 1672 tests, 0 failures.
- Mac scratch rsync to /tmp/bob-mac-capture-queued-code-return-expectations excluding .build/.git; ./Scripts/bundle.sh then just typecheck-tests passed (PASS BobMacCaptureTests, BobMacCaptureInstallHelperTests, CaptureCoreTests, RefsCoreTests; stub typecheck only). Scratch copy then removed. Never used Bryan's checkout or just install.
- sase bead epic-symbols bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.4: no entries (re-run after check).
- Primary bob-cli just check: sase tool run check 3f9ed094c0c00566e5dab81faaa05324, monitor 3yhrth8mxcx4, exit 0, triage verdict pass, KNOWN 0, FLAKY 0. bob-cli tree unchanged (clean master 96793fda).

Linked repo still needs host commit of RefsPanelModelTests.swift (dirty on 591e4fe). Real runtime verdict is master CI after that commit lands. Parent epic lander must inspect the run for the exact landed SHA (including later steps after lint), verify these queued-Return cases and the full suite, and only then close bob-cli-cr.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.4.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.4](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@f2513d2`](https://github.com/bobs-org/bob-mac-capture/commit/f2513d27b1a7a726ca426692103087e34535c144) | test(refs): correct queued-Return code picker expectations | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.4](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.4.md) | 2026-10-26 16:29:29 EDT |
