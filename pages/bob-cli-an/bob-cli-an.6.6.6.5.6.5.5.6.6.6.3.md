# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.3 — Show ledger progress, unblocked, and date marks in popout windows

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.3` · **Size:** small
**Created:** 2026-10-25 11:34:35 EDT · **Closed:** 2026-10-25 11:49:52 EDT
**Plan:** [202610/backlog\_batch11\_ref\_repair\_taskcard\_popout\_gkeep\_again.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch11_ref_repair_taskcard_popout_gkeep_again.md)

## Description

popout-mark-gates: resolve bob-cli-9q by making the bob-ledger-tools progress-mark, unblocked-glyph, and Tasks date-mark body-class gates hold in Obsidian popout windows for both toggle states, with tests and a bob plugins sync deploy.

## Notes

[2026-10-25T15:49:42Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.3] Work record (bob-cli-9q left OPEN for lander): baseline was main-window-only body classes in setup/toggle of 266/268/271. Fix: new shared BobLedgerToolsMarkGateMixin in src/266-plugin-mark-gate-mirror.js (markGateDocuments: main doc + markdown-leaf container docs + window-open-tracked popout docs; applyMarkGateClass; window-open sync reading live toggle state, resolving WorkspaceWindow.doc / win.document / window.document); 266/268/271 setups and toggles now call applyMarkGateClass + registerMarkGatePopoutSync; fragment registered in fragments.json and 310 install list; no CSS change (opt-in gates kept so toggle-off holds). Tests: new "mark gate holds in popout windows for both toggle states" in test-ledger-tools-{date,progress}-marks.cjs and test-ledger-tools-unblocked-glyph.cjs (failed 3/3 pre-fix, pass post-fix); full npm test 3669 pass; npm run validate 7/7 valid. Deployed via bob plugins sync --repo (bob-ledger-tools 1.69.0 copied to vault). Limitation: onunload still cleans only the main body (pre-existing; stale popout classes harmless since Obsidian removes plugin CSS on unload).

[2026-10-25T15:49:46Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.3] PROPOSED FOLLOW-UP: body.bob-priority-marks positive gate in styles.css likely hides priority marks in popout windows the same way bob-cli-9q did -- 265-plugin-priority-marks.js still adds the class to the main-window body only

[2026-10-25T15:49:52Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.3] Popout mark gates done: 3 new popout tests failed pre-fix and pass post-fix; full npm test 3669/3669 pass; npm run validate 7/7; bob-ledger-tools 1.69.0 rebuilt and deployed via bob plugins sync. bob-cli-9q left open for the lander; no ancestor closed.

## Dependencies

- **Depends on:** [bob-cli-an.6.6.6.5.6.5.5.6.6.6.2](bob-cli-an.6.6.6.5.6.5.5.6.6.6.2.md) ✓ · ⧖ 2026-10-25
- **Blocks:** [bob-cli-an.6.6.6.5.6.5.5.6.6.6.5](bob-cli-an.6.6.6.5.6.5.5.6.6.6.5.md) ◐ · ⧖ 2026-10-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.3/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.3](bob-cli-an.6.6.6.5.6.5.5.6.6.6.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@4e54e2f`](https://github.com/bobs-org/bob-plugins/commit/4e54e2f202c085a92c05ddfe8d81c49eb65ab297) | fix(ledger-tools): mirror mark gate body classes into Obsidian popout windows | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.3](bob-cli-an.6.6.6.5.6.5.5.6.6.6.3.md) | 2026-10-25 11:50:41 EDT |
