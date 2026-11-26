# Bead: bob-cli-q4.10.1 — Navigation gestures settle their written notes

[Bead Pages](../README.md) / [bob-cli-q4.10](bob-cli-q4.10.md) / bob-cli-q4.10.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q4.10](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q4.10.md) · **Assignee:** `bob-cli-q4.10.1.land`
**Created:** 2026-11-25 14:29:09 EST · **Closed:** 2026-11-26 04:51:51 EST
**Plan:** [202611/navigation\_gesture\_settle.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/navigation_gesture_settle.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/navigation_gesture_settle.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/navigation_gesture_settle.md

<!-- sase:links:end -->

## Description

Complete bob-cli-q4.10 by making every in-scope navigation status or residence write settle its touched notes atomically while preserving undo, task identity, cursor policy, review-walk behavior, and cross-note safety.

## Notes

[2026-11-25T22:34:11Z · bob-cli-q4.9.1.land] DISCOVERED ISSUE (from bob-cli-q4.9.1 land): nav settle jumps are recorded in the reverse order, and nav records a second jump for pending work the cycler owns. (1) navSettleJumpLocations (plugins/bob-navigation-hotkeys/src/181a-nav-task-settle.js:497) returns origin=outcome.cursor and destination=jumpTarget, and consumeNavSettleFlushResults passes them to recordJump(origin, destination). With the real nav history (recordVimJumpTransition, plus refreshVimJumpCurrentLocation on Ctrl+O, 090-local-task-ids.js), a stay-cursor settle recorded this way leaves the history at [stay, stay], so the first Ctrl+O does not move instead of reaching the moved task (approved settle_cursor=stay contract). The cycler records recordJump(from=jumpTarget, to=cursor). That order gives [moved, stay], and the first Ctrl+O lands on the moved task. Measured with real nav helpers at bob-plugins 7d53d189: cycler order -> Ctrl+O lands on line 20 (moved); nav order -> line 8 (no-op). The nav-only stay test (test-navigation-task-settle-adapter.cjs:380) asserts the jump count but not the order. (2) flushPendingNavSettles records jumps for every flushed pending outcome, but nav never calls schedulePending. Since q4.9.1.4 (cycler 1.64.0), Alt+]/Alt+[ arms provider pending settle with an onSettled observer (ledger-tools 1.163.0+) that already records the stay jump. Any wrapped nav command run within the ~500 ms burst therefore records the same settle twice in opposite orders: history [moved, stay, stay], so the first Ctrl+O does not move. Suggested remediation: record from=jumpTarget, to=cursor in navSettleJumpLocations, and leave pending-flush jumps to the scheduling consumer's onSettled (consume flush results without recordJump). Add an order assertion against real recordVimJumpTransition. Scope belongs to nav (this epic is mid-flight in 181a/181b), so the q4.9.1 lander did not edit nav. Also observed: master 0e8c70b7 (q4.10.1.4) committed nav src without a rebuilt main.js. npm run build:check reports a stale bob-navigation-hotkeys bundle, and npm run test:unit fails 3 nav tests (test-navigation-inbox-route.cjs:699, test-navigation-task-split-carry-api.cjs:440/461). After a local rebuild, test-navigation-task-split-carry-api.cjs:638 (splitRequirementCarry cross-note Undo) still fails.

[2026-11-26T07:01:33Z · bob-cli-q8.land] DISCOVERED ISSUE (from bob-cli-q8 land; corroborates PROPOSED FOLLOW-UPs on bob-cli-q8.5 #1, q8.6 #1, q8.8 #1): 21 bob-plugins test:unit failures that start with this epic's settle work. They reproduce identically on detached worktrees at ec93b88c (q4.10.1.5, before any q8 plugin commit) and at master d1a25d90: scripts/test-navigation-blocks-stage-view.cjs 11 (showBlocksStage CURRENT/RESULTS counts 0 vs 1, RBU4 footer verb, RBU5 subtitle, RBG5 stale refuse, 'Cannot read properties of undefined (reading view)', 'Cannot set properties of undefined (setting lastReason)', RBP11, Tab CURRENT removal); scripts/test-navigation-dependency-link-consumption.cjs 7 (PDL8-PDL10, applyDependencyEdit removes one live link / keeps the dependent write on daily preimage change / zero cachedReads: all {ok:false, reason:'commit-failed'}; same-note marked, counted vault and counted ^prj consumption counts); scripts/test-navigation-dependencies-stage-writes.cjs:735 (Tab same-note + cross-note CURRENT removals in one vault batch: 1 !== 2). Likely root cause: these harnesses never bind the active markdown editor that settled writers now resolve. ec93b88c added bindActiveMarkdownEditor(plugin, editor, path) to test-navigation-dependencies-writer.cjs but not to these files, and the q8 lander's identical one-line binding fixed q8's own DW20-DW22 'commit-failed' failures in that file. Repro: cd bob-plugins && node --test scripts/<file>.cjs.

[2026-11-26T09:51:51Z · bob-cli-q4.10.1.land] LANDED (bob-cli-q4.10.1 land agent, 2026-11-26).

VERIFIED
- All six phases are closed with evidence. The source matches their notes. 181a-d holds the guarded taskSettle v1 consumer: feature detection; missing, old, or throwing providers fall back; path and preimage guards hold; restore never settles; annotated writes keep BLOCKS_MACHINE_WRITE_ANNOTATION. Command flush wraps every registered bob-navigation-hotkeys:* callback (checkCallback only when checking !== true), Vim defineActions, physical routes, and the public-API subset.
- Lane, freshness, decay, cancel (510/520/530/540/548/550), card, priority, and schedule commits (390/450/560 via applyNavGesturePostimage, 570/580/610), moves (615/642/650), split persistence (653/656), inbox route (655), dependency and relation writers (420/430/580/592/594/600/600b), and project subtree writers (218/219) all stage full postimages through the adapter. Generated mirror-only and LINKS-only writes stay status-neutral.
- DECISIONS held. settle_cursor=stay: the cursor keeps its line and one jump is recorded from the settled task to the stay cursor. o_in_group=intake_end: scaffold insertion is untouched. memory_settle_record=no: no sase/memory edits. fc9c91ca touched only docs/develop/decisions.md, a docs-gate repair. wasm_spike is left to the bob-cli-q4 lander.
- Epic note #1 (q4.9.1 land) is addressed. navSettleJumpLocations now returns origin=jumpTarget, destination=cursor, and flushPendingNavSettles consumes results with recordJump:false. The adapter tests assert from/to order and that the scheduler jump is not duplicated. The stale nav bundle and the split-carry Undo failure are fixed (24dbb8a1, 8645ed55).
- Epic note #2 (q8 land, 21 harness failures) is addressed. Phase 6 bound the active editor in the stage and consumption harnesses, and those suites pass.
- Gates: bob-plugins npm test at master 8645ed55 passes build:check, docs inventory up to date, unit 9817 pass / 0 fail / 4 skip, perf 26/26.
- Deployment: bob-navigation-hotkeys 2.107.11 is synced on athena from 8645ed55. The bob-cli docs/reference/plugins/bob-navigation-hotkeys.md copy is byte-identical to bob-plugins docs, settle section included.
- sase bead epic-symbols reports no entries for bob-cli-q4.10.1 or bob-cli-q4.10.

INTEGRATED
- Reviewed the 48 bob-plugins commits since f224bc72 that are not epic commits.
- The q8 tie work composes inside the settled boundaries: 087/088 absorption, 596 applyTieChange delegating to applyDependencyEdit/applyBlocksEdit/applyRelationEdit, same-note reversal through one settled annotated transaction, and counted/vault absorption in 270/420 folded before navApplySettledEditorPostimage. Cross-note tie follow-ups drop plain links only, which is status-neutral. Commands added after phase 1 (tie chords) are covered by the registry-wide flush wrapper.
- q4.9.1 cycler pending settle and onSettled jumps coexist with nav flush and do not double-record.
- The bob-cli commits since the epic started are CLI, docs, and snooze work that needs no nav change.
- Recorded boundary, not a gap: the obsidian://bob-goto-task and bob-open-notes protocol handlers (490) do not flush pending settles. They fall outside the plan's flush inventory (commands, Vim, physical keys, plugin public APIs). Landing resolves by block ID, and later pending settles map other cursors through the settle map.
- No integration edits were needed.

FOLLOW-UP TRIAGE
- q4.10.1.6 #2 (cycler open-line wall clock): declined as already fixed by 2cad24b7 (q8.10.3). The test passes in today's full suite. Recorded on bob-cli-q4.
- q4.10.1.6 #3 (98 bob-cli just check failures): not caused by this epic, which changed no Rust. I reproduced it fresh at ae78dbb2: lib 43 and CLI 55 failures. 80 are drawer-cutover drift, noted on active epic bob-cli-ph. 17 are settle-drift nodes, noted on active epic bob-cli-q4. 1 is wispr, +1 on bob-cli-q9. No new task.
- q4.10.1.6 #4 (full-vault gate blocked by block-id-prompt, bob-ledger-tools, and task-status-cycler drift): not caused by this epic. Those plugins carry undeployed bob-cli-ph.10 (fda0ef27/2ba3315d) and bob-cli-pl.9.1.2 commits. DISCOVERED ISSUE notes added on bob-cli-ph and bob-cli-pl. Not deployed here because this delegated scope is nav-only and -F is forbidden. No new task.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q4.10.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.10.1.land/README.md) | [bob-cli-q4.10.1](bob-cli-q4.10.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli--plans | [`bob-cli--plans@7b9d46e`](https://github.com/bobs-org/bob-cli--plans/commit/7b9d46eae424f1c2dc67d8fff1b60bf82a29162a) | chore(plans): mark navigation gesture settle epic done | [bob-cli-q4.10.1](bob-cli-q4.10.1.md) | 2026-11-26 04:53:03 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q4.10.1.1][1] | Need epic DECISIONS and phase list for settle-bridge | 2 |
| read-by | [agent:bob-cli-q4.10.1.2--1][2] | Need parent epic decisions and phase history before continuing | 1 |
| read-by | [agent:bob-cli-q8.land][3] | Lander q8: check whether settle epic already tracks plugin harness test failures | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.10.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q4.10.1.2.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q8.land/README.md

<!-- sase:referenced-by:end -->
