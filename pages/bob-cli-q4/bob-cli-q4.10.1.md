# Bead: bob-cli-q4.10.1 — Navigation gestures settle their written notes

[Bead Pages](../README.md) / [bob-cli-q4.10](bob-cli-q4.10.md) / bob-cli-q4.10.1

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q4.10](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q4.10.md) · **Assignee:** `bob-cli-q4.10.1.land`
**Created:** 2026-11-25 14:29:09 EST
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

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q4.10.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.10.1.land/README.md) | [bob-cli-q4.10.1](bob-cli-q4.10.1.md) | 0 |

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
