# Bead: bob-cli-2v.3 — CaptureCore task-link picker index, source, and decoding

[Bead Pages](../README.md) / [bob-cli-2v](README.md) / bob-cli-2v.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.3j](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.3j.md) · **Assignee:** `bob-cli-2v.3` · **Size:** medium
**Created:** 2026-09-30 13:00:14 EDT · **Closed:** 2026-09-30 13:32:46 EDT
**Plan:** [202609/task\_link\_picker.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/task_link_picker.md)

## Description

mac_core: in bob-mac-capture's CaptureCore, decode the new candidate fields and add the `taskLink` picker source and need. Add `TaskLinkPickerIndex` with grouped and fuzzy-filtered presentations, rows keyed by route and ref, and a `:`-aware FuzzyQuery. Cover it with unit tests and verify on macOS CI.

## Notes

[2026-09-30T17:31:21Z · bob-cli-2v.3--1] Verification evidence: just format-lint GREEN and just build GREEN on macOS (Build complete). New TaskLinkPickerIndex logic verified on macOS via standalone harness against compiled CaptureCore: 35/35 checks passed (decoding of note_kind/block_id_suggestions/group/scheduled/pulls_forward + tolerant defaults, grouped order/titles/route|ref keys, dedupe, filtered ranking incl. colon-seed queries, ID-less pending rows, schedule/pull-forward and action lines, FuzzyQuery sigils). just test (swift test) is RED but purely environmental: every test target fails with no such module XCTest on this CLT-only mac host (no full Xcode, no XCTest.framework in SDK); reproduced identically on the clean base tree via git stash, including untouched test files.

[2026-09-30T17:31:28Z · bob-cli-2v.3--1] PROPOSED FOLLOW-UP: just test (swift test) fails on CLT-only mac hosts with no such module XCTest for all test targets, identically on the clean base tree; run the bob-mac-capture suite under full Xcode 26+ or macOS CI where XCTest exists, then close out TaskLinkPickerPresentationTests there.

[2026-09-30T17:32:46Z · bob-cli-2v.3--1] mac_core verified: just format-lint GREEN, just build GREEN on macOS; TaskLinkPickerIndex logic 35/35 harness checks GREEN against compiled CaptureCore on macOS. just test RED solely from missing XCTest on the CLT-only mac host, reproduced identically on the clean base tree (recorded as PROPOSED FOLLOW-UP for full-Xcode/CI run).

## Dependencies

- **Blocks:** [bob-cli-2v.5](bob-cli-2v.5.md) ◐ · ⧖ 2026-09-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2v.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-2v.3.md) | [bob-cli-2v.3](bob-cli-2v.3.md) | 0 |
