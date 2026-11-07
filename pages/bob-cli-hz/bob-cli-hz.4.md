# Bead: bob-cli-hz.4 — Fast == escape in the editor and picker

[Bead Pages](../README.md) / [bob-cli-hz](README.md) / bob-cli-hz.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.198](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.198.md) · **Assignee:** `bob-cli-hz.4` · **Size:** medium
**Created:** 2026-11-06 12:50:21 EST · **Closed:** 2026-11-06 19:45:03 EST
**Plan:** [202611/relation\_equals\_alias\_and\_direction\_flips.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/relation_equals_alias_and_direction_flips.md)

## Description

equals-escape: one shared equals-gesture record with a ~350 ms key-to-key window, so a fast second `=` undoes whatever the first `=` did and types one `=`. Covers the editor before and after Bob replies, every flip, and the picker; the card reuses it.

## Notes

[2026-11-07T00:45:03Z · bob-cli-hz.4] Equals-escape implemented in bob-mac-capture (shared CaptureEqualsGestureArm record, fast-== undo in editor/picker/card, before-reply ==/=~ probe, opener subtitle, docs, 15 new tests). Verified: just portable-check green (2261 tests), just docs-check green, epic-symbols clean. macOS UNVERIFIED: typecheck-tests started twice on mac scratch /tmp/bob-mac-check-hz4 (reached [8/18]) but the mac went unreachable mid-build and stayed dark; focused suites never ran. Monitor m8sqx8 left polling to finish the mac typecheck when the mac wakes; land agent must confirm macOS CI green.

[2026-11-07T01:55:13Z · bob-cli-hz.4--2] macOS verification status: mac typecheck-tests passed on scratch /tmp/bob-mac-check-hz4 (run cehg9x, exit 0). Focused suites (CaptureRelationEqualsAliasTests, CaptureRelationFlipAliasTests, CaptureRelationPanelTests, CaptureEqualsGestureTests) never ran: mac unreachable across repeated probes, monitor r9e5nw still staged/pending with no output. macOS targets remain unverified; scratch copy left in place for the pending run.

[2026-11-07T02:25:58Z · bob-cli-hz.4--3] macOS verification update: typecheck-tests passed on scratch /tmp/bob-mac-check-hz4 (run cehg9x, exit 0). Focused suites FAILED environmentally, not on code (run r9e5nw, exit 1): `swift test` via Scripts/xcode-swift.sh dies at import time with `no such module XCTest` in Tests/BobMacCaptureInstallHelperTests/InstallHelperArgumentsTests.swift, a target this phase never touched (clean tree, phase commit 4fbbe84; that target last changed in older commits). This mac has Command Line Tools without real XCTest, so no `swift test` suite can link/run there -- typecheck-tests.sh documents exactly this CLT case and passes via its XCTest stub. CaptureEqualsGestureTests (CaptureCoreTests, portable) already ran green in just portable-check (2261 tests, 0 failures). The three BobMacCaptureTests suites (CaptureRelationEqualsAliasTests, CaptureRelationFlipAliasTests, CaptureRelationPanelTests) are macOS/AppKit-only and unrunnable both here and on Linux; land agent must confirm macOS CI green before landing. Mac probed unreachable after the run, so scratch /tmp/bob-mac-check-hz4 is left in place.

[2026-11-07T03:26:01Z · bob-cli-hz.4--4] PROPOSED FOLLOW-UP: the three BobMacCaptureTests suites (CaptureRelationEqualsAliasTests, CaptureRelationFlipAliasTests, CaptureRelationPanelTests) need a full-Xcode mac or GitHub macOS CI because swift test cannot link on a CLT-only mac and the typecheck-tests stub is the max gate there. Mac typecheck-tests passed on scratch /tmp/bob-mac-check-hz4 in run 8d0pn8dg6hjs (exit 0, re-synced tree); XCTest probe printed CLT_NO_XCTEST__swift_test_cannot_link_without_Xcode. Confirmed environmental: git diff 418604a 4fbbe84 -- Tests/BobMacCaptureInstallHelperTests/ is empty, so the no-XCTest swift-test failure is identical on the clean base tree. Portable CaptureEqualsGestureTests already green in just portable-check (2261 tests). Scratch left in place.

## Dependencies

- **Depends on:** [bob-cli-hz.3](bob-cli-hz.3.md) ✓ · ⧖ 2026-11-06
- **Blocks:** [bob-cli-hz.5](bob-cli-hz.5.md) ✓ · ⧖ 2026-11-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-hz.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hz.4.md) | [bob-cli-hz.4](bob-cli-hz.4.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hz.4--1][1] | Check notes before recording mac verification status | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hz.4.md

<!-- sase:referenced-by:end -->
