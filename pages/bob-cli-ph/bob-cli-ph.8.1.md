# Bead: bob-cli-ph.8.1 — Finish Bob Mac Capture true-case drawers

[Bead Pages](../README.md) / [bob-cli-ph.8](bob-cli-ph.8.md) / bob-cli-ph.8.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ph.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.8.md) · **Assignee:** `bob-cli-ph.8.1.land`
**Created:** 2026-11-25 20:55:59 EST · **Closed:** 2026-11-26 06:37:25 EST
**Plan:** [202611/finish\_mac\_true\_case\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_mac_true_case_drawers.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/finish_mac_true_case_drawers.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 4 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_mac_true_case_drawers.md

<!-- sase:links:end -->

## Description

Bob Mac Capture builds green again, draws Bob-annotated drawer headers as a tray plus the verbatim title, paints draft drawer titles and delimiters from Bob's spans, and types `*`, Backspace, newline, and overtype assists on Bob's authority, completing bob-cli-ph.8.

## Notes

[2026-11-26T09:02:22Z · bob-cli-ph.8.1.land] LAND TRIAGE of PROPOSED FOLLOW-UPs: (1) bob-cli-ph.8.1.3 #2 and bob-cli-ph.8.1.4 #1 (macOS Test-step bare fatalError) DECLINED: not pre-existing; the cited 'clean base 4d9e845' is this epic's own preview-tray commit 4d9e845e, whose test target failed to compile (DrawerHeaderDesignTests.swift:59/80, run 45753263190), and run 45763712398 failed compiling CaptureDrawerPipelineTests.swift ('cannot find model'); both fixed in-epic by c2dd7fbf and a2e79f65, and run 45780151440 now executes all 5297 tests. (2) bob-cli-ph.8.1.5 #1 (CaptureDrawerPipelineTests compile errors) DECLINED as a task: caused by this epic's c561b26a, fixed by a2e79f65. (3) bob-cli-ph.8.1.6 #2 (bob-cli just check red drawer goldens) not caused by this epic (ph.10 cutover 9573ff86/46aba677): ROUTED to active epic bob-cli-ph as corroboration of its note #4 / bob-cli-ph.10 #3; reproduced independently on 1c23bce7. (4) bob-cli-ph.8.1.6 #3 (Mac push, exact-SHA CI, screenshots) is EPIC WORK, carried into the lander tale. (5) Lander-discovered: Mac drawer preview fixtures predate the cutover (grammar 31, legacy_caps): ROUTED to bob-cli-ph as a DISCOVERED ISSUE (cutover drift, related to but not a duplicate of bob-cli-ge). (6) Lander-discovered integration conflict: 631a49d5 re-added legacy_caps to docs/task-drawers.md, already corrected by ph.10's 1d6df8d1; no further edit needed. REMAINING EPIC WORK: exact-SHA macOS run 45780151440 on a2e79f65 fails 7 CaptureDrawerPipelineTests (23 assertions; first CI execution of 8.1.4/8.1.5 tests), and the Mac drawer-menu docs keep stale ALL-CAPS examples.

[2026-11-26T11:37:25Z · bob-cli-ph.8.1.land--4] LAND VERIFIED. Phases closed: 8.1.1 annotation-build-repair, 8.1.2 preview-tray, 8.1.3 draft-styling, 8.1.4 star-expansion, 8.1.5 title-keys, 8.1.6 mac-acceptance (all CLOSED before this tale; PROPOSED FOLLOW-UP triage stands per epic note 1). Seven drawer pipeline tests landed via 3 Mac commits + 1 test-harness edit: PRODUCT fixes - caret placement after star/overtype assist replay in CapturePanelController (403781d2), dropped stale analysisGeneration guard in freshDrawerTitleAuthorization in CapturePanelModel (403781d2), drawer-newline undo isolation in CapturePanelController (b38c4cc), old-Bob tip race hardening (b38c4cc); TEST fixes - star/overtype expectations, drawer-scoped rewrite assertion, undo-boundary harness (breakUndoCoalescing + 80ms runloop yield), Swift-6 self-capture compile fix (ab98419 + working-tree yield). Green gate: https://github.com/bobs-org/bob-mac-capture/actions/runs/45806522346 snapshot SHA 3635cbfe169a86820f970ef09615ae573159e7d2 - Lint/Build/Test/Bundle/plist/launch-smoke/install all ok. Screenshots: 16 drawer-headers PNGs inspected and registered as file:explicit artifacts, refs attached to 8.1.6 and ph.8. Docs reconciled: docs/capture-panel.md + docs/task-pickers.md true-case (Notes/Future Work/Motivation/Acceptance/Perf Budget/#name/bold child bullets); docs lint ok, word budgets hold; just docs-check generated drift in bob-ledger-tools.md/index.md is pre-existing (untouched by this tale); just check-scripts 43 tests OK. No Rust/grammar, plugin, memory-note, or vault changes; no version/changelog edits. Working-tree test-harness yield commits via this turn finalizer; post-push exact-SHA watch staged separately.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ph.8.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.8.1.land.md) | [bob-cli-ph.8.1](bob-cli-ph.8.1.md) | 5 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@403781d`](https://github.com/bobs-org/bob-mac-capture/commit/403781d2b3d2921584b677fae1e76b4c5bfd952b) | fix(mac-capture): land true-case drawer pipeline tests and reconcile docs | [bob-cli-ph.8.1](bob-cli-ph.8.1.md) | 2026-11-26 04:28:54 EST |
| bob-mac-capture | [`bob-mac-capture@b38c4cc`](https://github.com/bobs-org/bob-mac-capture/commit/b38c4cc3ced036c644cc230158972b819ed3fcf3) | fix(mac-capture): isolate drawer newline undo and harden old-Bob tip race | [bob-cli-ph.8.1](bob-cli-ph.8.1.md) | 2026-11-26 05:05:39 EST |
| bob-mac-capture | [`bob-mac-capture@ab98419`](https://github.com/bobs-org/bob-mac-capture/commit/ab9841959e3032d478aa5d2f2ff6163c1c6984a5) | fix(mac-capture): qualify self capture in old-Bob tip wait | [bob-cli-ph.8.1](bob-cli-ph.8.1.md) | 2026-11-26 05:22:59 EST |
| bob-mac-capture | [`bob-mac-capture@5949d25`](https://github.com/bobs-org/bob-mac-capture/commit/5949d253f6a210f992096858e559e59c188682bd) | fix(mac-capture): isolate drawer title/newline undo with runloop yield | [bob-cli-ph.8.1](bob-cli-ph.8.1.md) | 2026-11-26 06:41:25 EST |
| bob-cli--plans | [`bob-cli--plans@b1fb0bb`](https://github.com/bobs-org/bob-cli--plans/commit/b1fb0bb4e3532225ec53905e0420940ceb910711) | docs(plans): mark finish\_mac\_true\_case\_drawers done | [bob-cli-ph.8.1](bob-cli-ph.8.1.md) | 2026-11-26 06:42:51 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ph.10][1] | Identify existing evidence or task tracking for baseline drawer fixture failures | 1 |
| read-by | [agent:bob-cli-ph.8.1.1--4][2] | Inspect the specified epic and its descendants before deciding whether closure is permitted | 1 |
| read-by | [agent:bob-cli-ph.8.1.land--2][3] | drawer land gate retry follow-up: need bead state and plan refs | 1 |
| read-by | [agent:bob-cli-ph.8.1.land--4][3] | Land tale: need phase bead status and scope for closures | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.10.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.8.1.1.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.8.1.land.md

<!-- sase:referenced-by:end -->
