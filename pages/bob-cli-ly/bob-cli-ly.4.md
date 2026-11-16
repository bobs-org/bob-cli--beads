# Bead: bob-cli-ly.4 — Panel wiring, keys, accept and open, truthful fixtures, Mac docs

[Bead Pages](../README.md) / [bob-cli-ly](README.md) / bob-cli-ly.4

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1cr](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1cr.md) · **Assignee:** `bob-cli-ly.4` · **Size:** medium
**Created:** 2026-11-15 16:47:01 EST
**Plan:** [202611/note\_goto\_double\_slash.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/note_goto_double_slash.md)

## Description

mac-note-panel: wire `note_goto` into the panel model and key router (continuation, peel, consume rules), open notes read-only, add generated fixtures and panel tests, document the picker, and land green on macOS CI.

## Notes

[2026-11-16T03:09:35Z · bob-cli-ly.4] PROPOSED FOLLOW-UP: Trim docs/reference/plugins/bob-ledger-tools.md below the 6,000-word reference cap; just docs-check fails only on its unchanged 6,281-word clean-base content.

[2026-11-16T03:14:59Z · bob-cli-ly.4] Handoff caution: the staged watcher resolves HEAD when it starts; because this turn carries the dirty linked checkout, a green result for the old HEAD does not verify these changes. Commit the carried tree, watch CI for that new exact SHA, and close only after it is green.

[2026-11-16T03:27:48Z · bob-cli-ly.4--1] PROPOSED FOLLOW-UP: Investigate CaptureDotRouteAliasTests.testFastDoubleDotBeforeReplyCollapsesToOne: CI run 43780481574 failed at the asks-count assertion on clean base SHA 19e4c4048a0e7bfbdc69eeb356ddb497481dca99, before the uncommitted Notes panel changes were included.

[2026-11-16T04:05:49Z · bob-cli-ly.4--3] CI follow-up: preflight run 43800683604 (https://github.com/bobs-org/bob-mac-capture/actions/runs/43800683604) tested snapshot SHA 656390050fc473b7337504958af5401fcc9360d0 from base 5bc9478f3322bbdcb4da52e72bcfba8e85b0e62f. Build passed; Test failed with only `error: fatalError`, no test name, no hang sample artifact, and no actionable stack in `gh run view --log-failed`. This differs from known clean-base run 43780481574, which completed 4,773 tests and failed only CaptureDotRouteAliasTests.testFastDoubleDotBeforeReplyCollapsesToOne. Recheck on the committed exact HEAD before close.

[2026-11-16T04:25:53Z · bob-cli-ly.4--4] macOS CI compile regression found in run 43802559714 (snapshot SHA d1ac712b1e82411c490f05e6a288ad95bca7ae49, base 5bc9478f3322bbdcb4da52e72bcfba8e85b0e62f): CaptureNoteGotoPanelTests.swift memberwise CaptureKeyRoutingContext arguments were out of declaration order, plus markerExists needed explicit self in an async closure. Fixed those test call sites. The earlier portable-check passed 2,512 tests with 1 skipped but does not type-check this Mac test target; post-commit portable, preflight, and exact-HEAD watcher are being staged. Phase remains open.

## Dependencies

- **Depends on:** [bob-cli-ly.2](bob-cli-ly.2.md) ✓ · ⧖ 2026-11-15
- **Depends on:** [bob-cli-ly.3](bob-cli-ly.3.md) ✓ · ⧖ 2026-11-15
- **Blocks:** [bob-cli-ly.5](bob-cli-ly.5.md) ◐ · ⧖ 2026-11-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ly.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ly.4.md) | [bob-cli-ly.4](bob-cli-ly.4.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@5bc9478`](https://github.com/bobs-org/bob-mac-capture/commit/5bc9478f3322bbdcb4da52e72bcfba8e85b0e62f) | feat(capture): open notes from the // Go To Notes picker | [bob-cli-ly.4](bob-cli-ly.4.md) | 2026-11-15 22:33:52 EST |
| bob-mac-capture | [`bob-mac-capture@d12cd6c`](https://github.com/bobs-org/bob-mac-capture/commit/d12cd6c7d94d61d300e102257e065eb17d8ad646) | fix(capture): compile Notes picker macOS tests | [bob-cli-ly.4](bob-cli-ly.4.md) | 2026-11-15 23:29:36 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ly.4--1][1] | Need the assigned phase scope, design path, and epic decisions while recovering the failed exact-SHA Mac CI run | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ly.4.md

<!-- sase:referenced-by:end -->
