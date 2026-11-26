# Bead: bob-cli-ph.8 — Bob Mac Capture drawer rendering and typing

[Bead Pages](../README.md) / [bob-cli-ph](README.md) / bob-cli-ph.8

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5x.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5x.linker.w0.md) · **Assignee:** `bob-cli-ph.8` · **Size:** large
**Created:** 2026-11-22 17:36:49 EST
**Plan:** [202611/true\_case\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/true_case_drawers.md)

## Description

mac-drawers: the Mac renders bob's drawer spans and preview annotations, dims the delimiters, drives the `*` assist through capture-rewrite, and stops uppercasing drawer titles.

## Notes

[2026-11-25T23:37:48Z · bob-cli-ph.8] Planning only: verified prerequisite bob-cli-ph.6 is closed and its Rust drawer contracts are present. Mac fc0d4551 still needs preview drawer annotation plumbing, title/delimiter styling, physical-star and span-driven typing assists, and removal of drawer uppercasing in transfer/merge presentations. Existing menu and sub-bullet title preservation is retained. Authored a medium tale covering implementation, fixtures, docs, and exact-SHA macOS verification; strict validation passed with zero warnings. No product source changed and no implementation attempted in this planning turn. Submitting through sase plan propose; keep this phase assigned until implementation and verification finish.

[2026-11-25T23:37:57Z · bob-cli-ph.8] PROPOSED FOLLOW-UP: Installed SASE lacks the documented on-demand roster selector — sase memory read roster:decisions -r ... exits with unknown memory web: roster on this host; sase memory read --help documents only flat/web/strand forms. Used sase memory web show decisions plus audited governing strand reads for this plan. Land agent should triage the runtime/instructions mismatch.

[2026-11-26T00:49:08Z · bob-cli-ph.8--2] Phase progress: regenerated true-case drawer fixtures from clean bob-cli 05dd83cf (bob 0.6.0, grammar 31) with BOB_BIN=target/debug/bob; fixed generate-drawer-fixtures.sh syntax (stray paren) and captured grammar_revision plus marker-aware self-checks; added CaptureDrawerAnnotation/marker models and plumbed optional drawer through CapturePomodoroBlockLine, CaptureBlockDiffRow, and task/pomodoro presentations; removed drawer .uppercased() in transfer/merge-in container labels; updated docs/task-drawers.md Mac section and Mac docs/protocol.md + capture-previews.md within word budgets. Gates: Mac check-scripts python tests pass (9 + 43 tests OK); primary just docs-check shows only the two pre-existing budget overages (capture-syntax 6086, json-outputs 6044) also present with Mac stashed; Mac docs now under budget after trimming. Remaining for a Mac-enabled host: BlockDiffCard tray branch, draft span styling, rewrite-driven star/Return/overtype/Backspace assists, portable + AppKit/SwiftUI regression tests, just portable-check, typecheck-tests, macos-ci-check exact-SHA run, then close.

[2026-11-26T00:49:19Z · bob-cli-ph.8--2] PROPOSED FOLLOW-UP: primary just docs-check reports pre-existing word-budget overages docs/reference/capture-syntax.md (6086/6000) and docs/reference/json-outputs.md (6044/6000); reproduced with Mac changes stashed so unrelated to this phase. Primary just check also fails on clippy manual_contains in tests/cli/capture/complete_block_id.rs:292 (ids.iter().any vs contains), a file this phase does not touch (primary diff is docs-only). No new beads created.

[2026-11-26T01:53:43Z · bob-cli-ph.8] Planning only (run 3): Mac master is RED since b45b1951 (CI run 45731912096): CaptureModels.swift:9857 CaptureDrawerSummary.init(from:) calls raw.map(CaptureDrawerMarker.init(wireValue:)) on a String, so the earlier landing was never compiled. Remaining scope (tray preview, draft span paint, star/Backspace/newline/overtype assists, tests, screenshots, exact-SHA CI) did not fit one agent, so authored a child epic: annotation-build-repair (small, no deps, urgent) -> preview-tray || draft-styling -> star-expansion -> title-keys -> mac-acceptance; land agent closes only bob-cli-ph.8. Embedded decision drawer_newline_keys because Mac plain Return captures (Shift/Option-Return and Ctrl-J are the newline keys). athena (Swift 6.0.3) and mac (CLT) were reachable at planning time. No product files changed this turn.

## Dependencies

- **Blocks:** [bob-cli-ph.11](bob-cli-ph.11.md) ◐ · ⧖ 2026-11-22
- **Depends on:** [bob-cli-ph.6](bob-cli-ph.6.md) ✓ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-pq.5](../bob-cli-pq/bob-cli-pq.5.md) ✓ · ⧖ 2026-11-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ph.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.8.md) | [bob-cli-ph.8](bob-cli-ph.8.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f4da72f`](https://github.com/bobs-org/bob-cli/commit/f4da72ff5dd08b9827eb8b13a9f2bce04c47d9f6) | docs(task-drawers): describe Mac thin-client drawer contract | [bob-cli-ph.8](bob-cli-ph.8.md) | 2026-11-25 19:51:53 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:1fk][1] | Research whether pq.3/pq.5 truly depend on bob-cli-ph | 1 |
| read-by | [agent:bob-cli-ph.8--1][2] | Confirm assigned scope and final decisions before completing the phase | 1 |
| read-by | [agent:bob-cli-ph.8--2][2] | Continue remaining Mac tray styling typing assists tests | 3 |
| read-by | [agent:bob-cli-pq.1][3] | sequencing check for glyph-contract | 2 |
| read-by | [agent:bob-cli-pq.3][4] | Check prerequisite Mac drawer implementation status | 1 |
| read-by | [agent:g1][5] | Check whether phase is blocked on the release gate | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.1fk/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.8.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pq.1/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pq.3/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.g1/README.md

<!-- sase:referenced-by:end -->
