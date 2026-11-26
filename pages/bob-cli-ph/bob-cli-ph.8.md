# Bead: bob-cli-ph.8 — Bob Mac Capture drawer rendering and typing

[Bead Pages](../README.md) / [bob-cli-ph](README.md) / bob-cli-ph.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5x.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5x.linker.w0.md) · **Assignee:** `bob-cli-ph.8` · **Size:** large
**Created:** 2026-11-22 17:36:49 EST · **Closed:** 2026-11-26 06:37:25 EST
**Plan:** [202611/true\_case\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/true_case_drawers.md)

## Description

mac-drawers: the Mac renders bob's drawer spans and preview annotations, dims the delimiters, drives the `*` assist through capture-rewrite, and stops uppercasing drawer titles.

## Notes

[2026-11-25T23:37:48Z · bob-cli-ph.8] Planning only: verified prerequisite bob-cli-ph.6 is closed and its Rust drawer contracts are present. Mac fc0d4551 still needs preview drawer annotation plumbing, title/delimiter styling, physical-star and span-driven typing assists, and removal of drawer uppercasing in transfer/merge presentations. Existing menu and sub-bullet title preservation is retained. Authored a medium tale covering implementation, fixtures, docs, and exact-SHA macOS verification; strict validation passed with zero warnings. No product source changed and no implementation attempted in this planning turn. Submitting through sase plan propose; keep this phase assigned until implementation and verification finish.

[2026-11-25T23:37:57Z · bob-cli-ph.8] PROPOSED FOLLOW-UP: Installed SASE lacks the documented on-demand roster selector — sase memory read roster:decisions -r ... exits with unknown memory web: roster on this host; sase memory read --help documents only flat/web/strand forms. Used sase memory web show decisions plus audited governing strand reads for this plan. Land agent should triage the runtime/instructions mismatch.

[2026-11-26T00:49:08Z · bob-cli-ph.8--2] Phase progress: regenerated true-case drawer fixtures from clean bob-cli 05dd83cf (bob 0.6.0, grammar 31) with BOB_BIN=target/debug/bob; fixed generate-drawer-fixtures.sh syntax (stray paren) and captured grammar_revision plus marker-aware self-checks; added CaptureDrawerAnnotation/marker models and plumbed optional drawer through CapturePomodoroBlockLine, CaptureBlockDiffRow, and task/pomodoro presentations; removed drawer .uppercased() in transfer/merge-in container labels; updated docs/task-drawers.md Mac section and Mac docs/protocol.md + capture-previews.md within word budgets. Gates: Mac check-scripts python tests pass (9 + 43 tests OK); primary just docs-check shows only the two pre-existing budget overages (capture-syntax 6086, json-outputs 6044) also present with Mac stashed; Mac docs now under budget after trimming. Remaining for a Mac-enabled host: BlockDiffCard tray branch, draft span styling, rewrite-driven star/Return/overtype/Backspace assists, portable + AppKit/SwiftUI regression tests, just portable-check, typecheck-tests, macos-ci-check exact-SHA run, then close.

[2026-11-26T00:49:19Z · bob-cli-ph.8--2] PROPOSED FOLLOW-UP: primary just docs-check reports pre-existing word-budget overages docs/reference/capture-syntax.md (6086/6000) and docs/reference/json-outputs.md (6044/6000); reproduced with Mac changes stashed so unrelated to this phase. Primary just check also fails on clippy manual_contains in tests/cli/capture/complete_block_id.rs:292 (ids.iter().any vs contains), a file this phase does not touch (primary diff is docs-only). No new beads created.

[2026-11-26T01:53:43Z · bob-cli-ph.8] Planning only (run 3): Mac master is RED since b45b1951 (CI run 45731912096): CaptureModels.swift:9857 CaptureDrawerSummary.init(from:) calls raw.map(CaptureDrawerMarker.init(wireValue:)) on a String, so the earlier landing was never compiled. Remaining scope (tray preview, draft span paint, star/Backspace/newline/overtype assists, tests, screenshots, exact-SHA CI) did not fit one agent, so authored a child epic: annotation-build-repair (small, no deps, urgent) -> preview-tray || draft-styling -> star-expansion -> title-keys -> mac-acceptance; land agent closes only bob-cli-ph.8. Embedded decision drawer_newline_keys because Mac plain Return captures (Shift/Option-Return and Ctrl-J are the newline keys). athena (Swift 6.0.3) and mac (CLT) were reachable at planning time. No product files changed this turn.

[2026-11-26T11:37:03Z · bob-cli-ph.8.1.land--4] Mac drawer acceptance screenshots verified. Green exact-SHA gate: https://github.com/bobs-org/bob-mac-capture/actions/runs/45806522346 snapshot SHA 3635cbfe169a86820f970ef09615ae573159e7d2 (Lint/Build/Test 5297 tests 0 failures/Bundle/plist/launch-smoke/install all ok). Inspected all 16 drawer-headers PNGs (edge+real x 620/760 x light/dark/high-contrast): tray distinct from checkbox and requirement diamond; true-case verbatim semibold titles (Requirements, Perf Budget; legacy FUTURE WORK as-sent); empty Drafts muted; removed Old Drawer struck+dimmed; no ** on drawer rows; **Just bold** stays verbatim; requirement Scope-it keeps diamond; long title wraps cleanly. Registered as file:explicit artifacts (16 refs attached).

[2026-11-26T11:37:40Z · bob-cli-ph.8.1.land--4] PHASE VERIFIED (closed with child epic 8.1 cascade). Scope complete: Mac renders Bob drawer spans + preview annotations (outline tray, verbatim true-case titles), dims delimiters with caret-adjacent full ink, drives star assist through capture-rewrite, stops uppercasing drawer titles; drawer_newline_keys = newline_keys final. Gates: green exact-SHA macOS run https://github.com/bobs-org/bob-mac-capture/actions/runs/45806522346 @ 3635cbfe169a86820f970ef09615ae573159e7d2 (Lint/Build/Test 5297x0/Bundle/plist/launch/install); 16 drawer-headers PNGs inspected, registered as file:explicit artifacts, refs attached here and on 8.1.6; epic-symbols clean on 8.1 and ph.8; docs reconciled (capture-panel.md/task-pickers.md). bob-cli just symvision + plan status follow from bob-cli checkout. Containing epic bob-cli-ph left open for its own lander; ph.8 notes 2/4 PROPOSED FOLLOW-UPs belong to bob-cli-ph lander.

## References

- file:explicit:92ac260b4e11d2084e051d00
- file:explicit:8cf8d08357d505985cc67004
- file:explicit:5922d9f1d9d98925f294a512
- file:explicit:57de71e8ea3f5dfdd5a934a5
- file:explicit:ce0a9003fdbdfdde5cb94511
- file:explicit:6d35dc2d9c381c63545fba03
- file:explicit:44ec5c8cb0a0d2c38aa6a3de
- file:explicit:719de2e5996765b69febd0f5
- file:explicit:8264c29c8718f9462fc51b5e
- file:explicit:15c959fa575be4f8bc1408f5
- file:explicit:22075c1c60e8fbe071b26a35
- file:explicit:08ba10fc00da9e997f951646
- file:explicit:180759c7af703517f7b40435
- file:explicit:59ba2549dd929ad4a04196da
- file:explicit:8c8d339af7b68f9fa19bdf3b
- file:explicit:0ba25b1607cc2ca3dde68e7a

## Dependencies

- **Blocks:** [bob-cli-ph.11](bob-cli-ph.11.md) ✓ · ⧖ 2026-11-22
- **Depends on:** [bob-cli-ph.6](bob-cli-ph.6.md) ✓ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-pq.5](../bob-cli-pq/bob-cli-pq.5.md) ✓ · ⧖ 2026-11-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ph.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.8.md) | [bob-cli-ph.8](bob-cli-ph.8.md) | 3 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@4eb9b2e`](https://github.com/bobs-org/bob-mac-capture/commit/4eb9b2e977dc8275a5849d5ac7f8bc8fabb617b2) | fix(mac): require grammar 30 for drawer fixtures | [bob-cli-ph.8](bob-cli-ph.8.md) | 2026-11-25 19:18:09 EST |
| bob-cli | [`f4da72f`](https://github.com/bobs-org/bob-cli/commit/f4da72ff5dd08b9827eb8b13a9f2bce04c47d9f6) | docs(task-drawers): describe Mac thin-client drawer contract | [bob-cli-ph.8](bob-cli-ph.8.md) | 2026-11-25 19:51:53 EST |
| bob-mac-capture | [`bob-mac-capture@b45b195`](https://github.com/bobs-org/bob-mac-capture/commit/b45b1951b0f983edc4d8e9deae5ad92e96bb00ab) | feat(mac): carry true-case drawer annotations from Bob | [bob-cli-ph.8](bob-cli-ph.8.md) | 2026-11-25 19:53:07 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:1fk][1] | Research whether pq.3/pq.5 truly depend on bob-cli-ph | 1 |
| read-by | [agent:bob-cli-ph.8--1][2] | Confirm assigned scope and final decisions before completing the phase | 1 |
| read-by | [agent:bob-cli-ph.8--2][2] | Continue remaining Mac tray styling typing assists tests | 3 |
| read-by | [agent:bob-cli-ph.8.1.land--4][3] | Confirm phase closure state after epic cascade close | 2 |
| read-by | [agent:bob-cli-pq.1][4] | sequencing check for glyph-contract | 2 |
| read-by | [agent:bob-cli-pq.3][5] | Check prerequisite Mac drawer implementation status | 1 |
| read-by | [agent:g1][6] | Check whether phase is blocked on the release gate | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.1fk/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.8.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.8.1.land.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pq.1/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pq.3/README.md
[6]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.g1/README.md

<!-- sase:referenced-by:end -->
