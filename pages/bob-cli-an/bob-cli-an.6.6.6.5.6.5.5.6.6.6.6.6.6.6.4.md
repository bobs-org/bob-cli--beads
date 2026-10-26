# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.4 — Turn bob-mac-capture master CI green on the queued code-key XCTest

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.4

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.4` · **Size:** large
**Created:** 2026-10-26 15:53:09 EDT
**Plan:** [202610/backlog\_batch15\_vault\_safety\_pdf\_moves\_and\_red\_gates.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch15_vault_safety_pdf_moves_and_red_gates.md)

## Description

mac-code-key-ci: resolve bob-cli-cr by deciding whether the queued-Return code picker regressed or its expectation is outdated, and fixing that side without weakening assertions.

## Notes

[2026-10-26T20:02:33Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.4] ROOT CAUSE BEFORE EDITS: bob-mac-capture is clean at 591e4fe. The approved plan:202610/ref_code_block_copy.md Initial selection contract explicitly says without a page select block 1. RefsCodePicker.initialSelection (Sources/RefsCore/RefsCode.swift) returns index 0 for nil page, with an existing portable test for that rule; c7a5f37 did not change it. That same commit introduced both testQueuedCodeKeyCopiesWhenCatalogReturns, which opens the ordinary library card without a Highlights Tabs page, and refs-code.json, whose block 1 is makefile/build (3 lines) and block 2 is yaml/refresh (14 lines, page 7). RefsCopyCard.codeLoaded resolves the pending picker and replays queued Return against its initial selection. Therefore the reported makefile copy is the approved behavior and the YAML expectation is incorrect for this setup. Plan a bounded test correction retaining exact payload/HUD assertions, with an explicit page-7 case to retain YAML coverage; no production policy or fixture-order change is justified. Phase had no earlier work notes; epic-symbols currently reports no entries. Implementation and phase closure will follow the required plan handoff; bob-cli-cr remains for the epic lander to close after landed-SHA macOS CI.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.4.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.4](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.4.md) | 0 |
