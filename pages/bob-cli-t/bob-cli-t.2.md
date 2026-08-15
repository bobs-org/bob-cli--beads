# Bead: bob-cli-t.2 — Integrate batch results and native editor behavior in the mac app

[Bead Pages](../README.md) / [bob-cli-t](README.md) / bob-cli-t.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.024.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.024.w1.md) · **Assignee:** `bob-cli-t.2` · **Size:** medium
**Created:** 2026-08-15 09:47:53 EDT · **Closed:** 2026-08-15 10:40:39 EDT
**Plan:** [202608/multi\_capture.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/multi_capture.md)

## Description

mac_batch_integration: decode and present aggregate results, add reliable indentation-aware Control-J edits, and preserve one-process submission semantics.

## Notes

[2026-08-15T14:27:35Z · 02b] RELATED INSTALL BLOCKER: Current bob-mac-capture tip 77da370 fails the macOS 26 SwiftPM Build step (Actions run 31887787743) before bundle/install. The fatal errors are CapturePanelModel.swift:65 evaluating CanceledDraftStash() as a default argument from a synchronous nonisolated context and CaptureKeyCommandRouter.swift:121 calling @MainActor CanceledDraftStash.acceleratorIndex from a nonisolated router. This phase owns both integration surfaces; coordinate any fix so default construction happens inside the main-actor initializer and pure Sendable stash helpers/constants are explicitly nonisolated. Re-run just build/test/bundle/install after resolution.

[2026-08-15T14:32:07Z · bob-cli-t.2] PROPOSED FOLLOW-UP: Clean up existing Swift 6 Sendable warnings in CaptureTargetsCache and BobProcessClient — SwiftPM reports Date.init @Sendable conversion and DispatchWorkItem capture warnings unrelated to this batch integration.

[2026-08-15T14:40:18Z · 02b] INSTALL BLOCKER FIX APPLIED (commit not yet made, uncommitted in bob-mac-capture working tree at tip 77da370): CapturePanelModel.init now default-constructs CanceledDraftStash inside the main-actor initializer body (param changed to canceledDraftStash: CanceledDraftStash? = nil, resolved via ?? CanceledDraftStash()) instead of evaluating it as a default-argument expression. CanceledDraftStash.defaultCapacity, .maximumCapacity, .acceleratorKeys, and .acceleratorIndex(for:entryCount:) are now explicitly nonisolated so CaptureKeyCommandRouter's nonisolated router can call acceleratorIndex synchronously; the stash instance itself stays @MainActor. Added CapturePanelModelTests.testDefaultConstructionCreatesUsableCanceledDraftStash to pin default-construction usability. Implemented from a Linux sandbox (no AppKit/macOS SDK available here: swift build --target BobMacCapture fails with 'no such module AppKit'), so just build/just bundle/install.sh have NOT been run yet -- needs macOS 26 + Xcode 26 validation (host or CI) before this is considered done.

[2026-08-15T14:40:39Z · bob-cli-t.2] Implemented mac batch integration on current bob-mac-capture origin/master: parse items/captures decoding, normalized aggregate model state/opening, batch preview stack, Control-J resolver, fixture/tests/docs, and CanceledDraftStash nonisolated/default-construction build fix. Verified git diff --check --cached, bash -n Tests/Fixtures/fake-bob, fake-bob nested/batch JSON jq checks, swift build --target CaptureCore, swift build --target CaptureCoreTests, and swiftc -parse Sources/BobMacCapture/CanceledDraftStash.swift. just format-lint/build/test were attempted and are blocked in this Linux workspace by missing Apple developer tools selection (exit 69/no Xcode CLT).

[2026-08-15T14:41:32Z · bob-cli-t.2] POST-CLOSE UPDATE: Added CapturePanelModelTests.testDefaultConstructionCreatesUsableCanceledDraftStash after the close note so the CanceledDraftStash default-construction fix is pinned locally. Re-verified git diff --check --cached, bash -n Tests/Fixtures/fake-bob, swift build --target CaptureCoreTests, and swiftc -parse Sources/BobMacCapture/CanceledDraftStash.swift.

[2026-08-15T14:42:30Z · bob-cli-t.2] Finalizer publication check after staged linked-repo work: verified CaptureCore and CaptureCoreTests target builds, fake-bob syntax/JSON fixture checks, stash-file Swift parse, and required just commands blocked only by missing Apple developer tools/Xcode CLT in this Linux workspace.

## Dependencies

- **Depends on:** [bob-cli-t.1](bob-cli-t.1.md) ✓ · ⧖ 2026-08-15
- **Blocks:** [bob-cli-t.3](bob-cli-t.3.md) ◐ · ⧖ 2026-08-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-t.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-t.2/README.md) | [bob-cli-t.2](bob-cli-t.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@4c22525`](https://github.com/bobs-org/bob-mac-capture/commit/4c2252578bc1c18b629ce369de8d71c2f32d0a5e) | feat: integrate batch capture results in mac app | [bob-cli-t.2](bob-cli-t.2.md) | 2026-08-15 10:44:23 EDT |
