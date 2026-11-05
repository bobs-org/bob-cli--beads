# Bead: bob-cli-he.4 — Mac Clip card shows provider and ages

[Bead Pages](../README.md) / [bob-cli-he](README.md) / bob-cli-he.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5r.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5r.linker.w0.md) · **Assignee:** `bob-cli-he.4` · **Size:** small
**Created:** 2026-11-05 10:29:53 EST · **Closed:** 2026-11-05 14:16:02 EST
**Plan:** [202611/percent\_c\_history\_agreement.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/percent_c_history_agreement.md)

## Description

mac-card: in bob-mac-capture, decode clip.history tolerantly, show provider and ages in the Clip card, and drop the Clipy wording from the panel docs.

## Notes

[2026-11-05T19:13:47Z · bob-cli-he.4] PROPOSED FOLLOW-UP: macOS CI Test step hangs at the 15-minute watchdog (stuck after WorkBadgeToneTests) on master, including the clean base commit 6e09f2c (run 42079206476) and this phase commit 9714a56 (run 42089082999); Lint and Build are green and all CaptureClipPresentationTests pass on macOS. Investigate the hanging test via the test-hang artifact.

[2026-11-05T19:16:02Z · bob-cli-he.4] Verified: swift build clean; full swift test 2177 passed/0 failed on Linux; all 12 CaptureClipPresentationTests (incl. 3 new provenance tests) pass on macOS CI with Lint and Build green; just docs-check passed. macOS CI Test step red via pre-existing 15-min watchdog hang after WorkBadgeToneTests, reproducing identically on clean base 6e09f2c (run 42079206476) vs this commit 9714a56 (run 42089082999); recorded as PROPOSED FOLLOW-UP. No epic-symbol leftovers.

[2026-11-05T19:37:52Z · bob-cli-he.4--1] PROPOSED FOLLOW-UP: macOS CI re-run for 9714a56 (run 42092346376) went red with 13 failed BobMacCaptureTests (CaptureSeparatorToggleTests x9, CapturePanelModelTests x2 comma tests, CaptureBackslashGotoTests x1, CaptureEditorWordMotionTests x1) plus the 15-min watchdog sample firing; same SHA earlier (run 42089082999) showed a hang after WorkBadgeToneTests with Clip tests passing instead. Failing files contain no clip/history references and 9714a56 touches only CaptureModels/CaptureClipPresentation+fixtures+docs, so these failures belong to the stacked separator/comma/backslash work (6e09f2c/6c39ff8/d206803/13e2f48/c95094d), not this phase; several failures are "Condition not met before timeout", suggesting a loaded runner. macOS-only target cannot be reproduced on Linux. Land agent triage requested; phase left untouched (tree clean at 9714a56).

[2026-11-05T19:39:10Z · bob-cli-he.4--1] PROPOSED FOLLOW-UP (base-tree evidence): the 13 red BobMacCaptureTests from run 42092346376 reproduce identically on clean base 6e09f2c (run 42079206476, event push, conclusion failure): stripped `gh run view --log-failed` error lines diff to identical (30 lines each; only the watchdog-echo timestamp differs). 9714a56 touches none of the failing files (only CaptureModels additive history, CaptureClipPresentation history branch, clip fixtures/tests, docs). Out of scope for this phase; triage to the separator/comma/backslash stack owners.

## Dependencies

- **Depends on:** [bob-cli-he.3](bob-cli-he.3.md) ✓ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-he.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-he.4.md) | [bob-cli-he.4](bob-cli-he.4.md) | 0 |
