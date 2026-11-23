# Bead: bob-cli-pq.6 — Mac previews, agenda, and Pull-In card draw the diamond

[Bead Pages](../README.md) / [bob-cli-pq](README.md) / bob-cli-pq.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1f8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1f8.md) · **Assignee:** `bob-cli-pq.6` · **Size:** medium
**Created:** 2026-11-23 03:54:18 EST · **Closed:** 2026-11-23 14:32:13 EST
**Plan:** [202611/task\_reqs\_criterion\_diamond.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_reqs_criterion_diamond.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:0c22af796820864312c80144 | attached via sase artifact create --bead |
| related | file:explicit:e56c77e214c8e923a7bb318b | attached via sase artifact create --bead |

<!-- sase:links:end -->

## Description

mac-diamonds: one SwiftUI requirement mark drawn from bob's state in the live preview, the idle agenda, and the Pull-In card rows, header, and filter, with staged-verdict flips, regenerated fixtures, and updated Mac docs.

## Notes

[2026-11-23T18:17:04Z · bob-cli-pq.6] Implemented Mac criterion marks in previews, idle agenda, and Pull-In rows/header/filter; additive req decoding, staged marks, compatibility/presentation tests, light/dark render fixtures, and docs are ready. RV vectors byte-copy verified. No epic-symbol entries. Remaining work fits one verification follow-up: regenerate response fixtures with a fresh Bob build, run scratch Mac bundle/typecheck-tests, portable checks, docs gates, bob-cli check, and exact-SHA macOS CI; then review results and close only this phase. SASE monitor will run these gates and resume this same agent; no implementation redesign or child epic needed.

[2026-11-23T18:24:38Z · bob-cli-pq.6--1] Verification recovery: the Rust build passed, but pq6-verify.sh used stale workspace target/debug/bob (0.5.0; --req-choice unsupported) while Cargo built 0.6.0 in its configured CARGO_TARGET_DIR. Fixed runner to derive the executable path from cargo metadata. Also fixed new provenance f-string braces and preserved fixture-command error output before cleanup. RV vectors remain byte-identical to primary. No Swift is committed; rerunning full verification through monitor, then inspect fixtures/docs drift and exact-SHA render artifacts and close this phase only.

[2026-11-23T18:58:31Z · bob-cli-pq.6--2] PROPOSED FOLLOW-UP: Repair the two pre-existing async assertions in Tests/BobMacCaptureTests/RefsPanelModelTests.swift:2916 and :2935 (testHighlightsTaskSecondCallWhileInFlightDrops and testHighlightsTaskPresentationDuringReadDrops). Clean Mac base c6c9c13e9353ce2dfdb3ed667e2ce916cbc30e91 CI run https://github.com/bobs-org/bob-mac-capture/actions/runs/45234472802 and our scratch typecheck from monitor 5f7rz9qkysfn report identical async-property-access-in-autoclosure errors. The test file is unchanged from HEAD. App bundle compilation passed; all three other test targets typechecked. No matching task found by exact test names/autoclosure search or recent CI-task sweep. This baseline failure must not block pq.6 closure under the user instruction; full exact-SHA phase CI will still run and its result must be compared. Evidence: .git/pq6-logs/baseline-evidence.txt; base CI job 137902408392.

[2026-11-23T19:27:44Z · bob-cli-pq.6--3] Exact-SHA verification corroboration: run https://github.com/bobs-org/bob-mac-capture/actions/runs/45247036039 at 1ca0fa231d1ca19cfa676ee89a25efd346f7bebf passed script checks, Swift formatting, and app Build. Its only unique compiler errors are the same RefsPanelModelTests.swift:2916/:2935 async XCTest autoclosure errors documented in PROPOSED FOLLOW-UP #3 and reproduced on clean base c6c9c13. Test stopped during compilation (not a watchdog hang). All Sources, Tests, and Scripts match the CI snapshot byte-for-byte, including the four new files. Render-fixtures download found no artifacts; requirement-states and requirement-pull-in visual inspection, native test execution, and the dependent bundle/signature/launch/install CI steps remain unverified. The scratch app bundle did compile. Documentation-only page-budget fixes are undergoing the final docs gate.

[2026-11-23T19:32:13Z · bob-cli-pq.6--3] Completed requirement diamonds in previews, idle agenda and Pull-In rows/header/filter, staged verdict marks, and Met with task wording; refreshed Bob 0.6.0 fixtures and provenance. Fixture review permits only glyph/scope/req annotations; legacy unchanged and RV vectors byte-identical. Scratch Mac app compilation, 2706 portable tests (one skipped), generator syntax, docs-gen, final docs-check (447 passed, one optional-font test skipped), bob-cli check, and whitespace checks passed. Fixed all three introduced documentation budget errors; primary docs generation produced no drift. Exact-SHA CI run 45247036039 (1ca0fa231d1ca19cfa676ee89a25efd346f7bebf) passed formatting and Build, then reproduced only the two clean-base RefsPanelModelTests async autoclosure errors already recorded as PROPOSED FOLLOW-UP. Sources/Tests/Scripts match that snapshot byte-for-byte. No introduced failures remain. Native test execution, render images, and dependent launch/install gates remain unverified because baseline compilation prevented them; user explicitly authorized closure for identical baseline failures. Evidence: file:explicit:0c22af796820864312c80144; final docs ToolRun de32c20626f28425cf94335562851f3a. Only this phase is closed; ancestors untouched.

## Dependencies

- **Depends on:** [bob-cli-pq.1](bob-cli-pq.1.md) ✓ · ⧖ 2026-11-23
- **Depends on:** [bob-cli-pq.2](bob-cli-pq.2.md) ✓ · ⧖ 2026-11-23
- **Depends on:** [bob-cli-pq.5](bob-cli-pq.5.md) ✓ · ⧖ 2026-11-23
- **Blocks:** [bob-cli-pq.7](bob-cli-pq.7.md) ◐ · ⧖ 2026-11-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-pq.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-pq.6.md) | [bob-cli-pq.6](bob-cli-pq.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@ff157b0`](https://github.com/bobs-org/bob-mac-capture/commit/ff157b0e4a680528d545aefc7d5d443752abd8a7) | feat(capture): draw requirement diamond and say Met with task | [bob-cli-pq.6](bob-cli-pq.6.md) | 2026-11-23 14:33:00 EST |
