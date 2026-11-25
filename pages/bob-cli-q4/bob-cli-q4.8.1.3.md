# Bead: bob-cli-q4.8.1.3 — Publish taskSettle v1 with the pending scheduler

[Bead Pages](../README.md) / [bob-cli-q4.8.1](bob-cli-q4.8.1.md) / bob-cli-q4.8.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q4.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q4.8.md) · **Assignee:** `bob-cli-q4.8.1.3` · **Size:** medium
**Created:** 2026-11-25 10:27:09 EST · **Closed:** 2026-11-25 13:40:51 EST
**Plan:** [202611/task\_settle\_twin.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_settle_twin.md)

## Description

pending-api: implement the shared 500 ms pending scheduler, early flush and teardown lifecycle, publish the complete taskSettle v1 namespace, document its consumer contract, verify skew and race behavior, and deploy bob-ledger-tools.

## Notes

[2026-11-25T17:55:05Z · bob-cli-q4.8.1.3--1] PROPOSED FOLLOW-UP: Reduce docs word-budget overages — docs:check fails on clean plugin base fdde3dcf against Bob CLI docs 0742684 with plugin-apis at 9287/8000 words and navigation-hotkeys at 6068/6000; current source is 9961/8000 and 6068/6000. The base run confirms both over-budget failures predate this phase.

[2026-11-25T18:40:22Z · bob-cli-q4.8.1.3--7] PROPOSED FOLLOW-UP: Reconcile the current docs:check word-budget failures. Latest run against the Bob Plugins source reports plugin-apis at 9961/8000, reference/capture-syntax at 6011/6000, reference/plugins/bob-ledger-tools at 6012/6000, and reference/plugins/bob-navigation-hotkeys at 6068/6000. The earlier clean-plugin-base comparison remains recorded above for plugin-apis and navigation-hotkeys; compare the current extra findings against that baseline before assigning them to this phase.

[2026-11-25T18:40:51Z · bob-cli-q4.8.1.3--7] Verified npm test passed (unit and performance suites; docs inventory current), npm run build:check passed, and bob plugins sync copied bob-ledger-tools successfully. sase bead epic-symbols reports no entries for this phase. npm run test:e2e:task-settle-undo passed in real Obsidian with taskSettle v1, confirming apply, joined/separate history handling, undo restoration, and redo restoration. npm run docs:check still reports word-budget failures (plugin-apis 9961/8000, capture-syntax 6011/6000, bob-ledger-tools 6012/6000, navigation-hotkeys 6068/6000); the current counts and prior clean-base comparison are recorded in PROPOSED FOLLOW-UP notes.

## Dependencies

- **Depends on:** [bob-cli-q4.8.1.2](bob-cli-q4.8.1.2.md) ✓ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q4.8.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q4.8.1.3.md) | [bob-cli-q4.8.1.3](bob-cli-q4.8.1.3.md) | 3 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@c945420`](https://github.com/bobs-org/bob-plugins/commit/c9454208ac8eede09f338c328ab640166ea3168e) | feat(ledger-tools): publish task settle v1 scheduler | [bob-cli-q4.8.1.3](bob-cli-q4.8.1.3.md) | 2026-11-25 12:35:32 EST |
| bob-plugins | [`bob-plugins@abbac5a`](https://github.com/bobs-org/bob-plugins/commit/abbac5acc380b651c091657d40f77d43680a9054) | test(ledger-tools): measure resident count cpu time | [bob-cli-q4.8.1.3](bob-cli-q4.8.1.3.md) | 2026-11-25 13:25:22 EST |
| bob-plugins | [`bob-plugins@84ba9d4`](https://github.com/bobs-org/bob-plugins/commit/84ba9d411c0f6692aba7bc19d26eea74ba8bb6b8) | test(bob-ledger-tools): measure frees-mark budget as CPU | [bob-cli-q4.8.1.3](bob-cli-q4.8.1.3.md) | 2026-11-25 13:31:05 EST |
