# Bead: bob-cli-ph.7.1.3 — Drawer marker typing and Toggle Drawer

[Bead Pages](../README.md) / [bob-cli-ph.7.1](bob-cli-ph.7.1.md) / bob-cli-ph.7.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ph.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.7.md) · **Assignee:** `bob-cli-ph.7.1.3` · **Size:** medium
**Created:** 2026-11-25 08:48:55 EST · **Closed:** 2026-11-25 11:20:47 EST
**Plan:** [202611/obsidian\_true\_case\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/obsidian_true_case_drawers.md)

## Description

drawer-typing: add scoped star expansion, Enter, overtype, atomic Backspace, undo, and Toggle Drawer beside the existing requirement typing assist.

## Notes

[2026-11-25T16:20:23Z · bob-cli-ph.7.1.3] PROPOSED FOLLOW-UP: Reconcile task-status-cycler fixtures with canonical Notes drawers. Clean-tree tests reproduce 10 assertions expecting NOTES while the writer emits **Notes** (req-toggle, open-line, task-reqs-vectors); those writer files are unchanged from the pre-phase tree, so this is outside drawer-typing scope.

[2026-11-25T16:20:31Z · bob-cli-ph.7.1.3] PROPOSED FOLLOW-UP: docs word budgets over base cap on clean tree. npm run docs:check fails identically without this work: plugin-apis.md 9287 words (cap 8000) and bob-navigation-hotkeys.md 6068 words (cap 6000); recorded clean-base, outside drawer-typing scope.

[2026-11-25T16:20:47Z · bob-cli-ph.7.1.3] Drawer typing implemented and verified: scoped star expansion to - **** (autopair on/off identical, one Undo returns - *), title-end overtype, atomic Backspace, smart Enter nested bullets, and Toggle Drawer command (wrap/unwrap, legacy ALL-CAPS marks bold without recasing, actionable refusal notices). New suite test-task-status-cycler-drawer-typing.cjs 21/21 pass; req-typing/twin-copies/settle suites pass; broader cycler sweep 1067/1077 with only the 10 documented clean-base NOTES failures (reproduced identically on clean tree). npm run build, build:check, validate, docs:inventory:check pass; deployed task-status-cycler via per-plugin sync. Two clean-base failures recorded as PROPOSED FOLLOW-UP notes.

## Dependencies

- **Depends on:** [bob-cli-ph.7.1.2](bob-cli-ph.7.1.2.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-ph.7.1.4](bob-cli-ph.7.1.4.md) ✓ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ph.7.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.7.1.3/README.md) | [bob-cli-ph.7.1.3](bob-cli-ph.7.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@8d3c555`](https://github.com/bobs-org/bob-plugins/commit/8d3c555c61041065281b74259086b82633719c47) | feat(task-status-cycler): add drawer marker typing and Toggle Drawer | [bob-cli-ph.7.1.3](bob-cli-ph.7.1.3.md) | 2026-11-25 11:21:53 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ph.7.1.3][1] | Need full details including notes and decisions | 2 |
| read-by | [agent:bob-cli-ph.7.1.4][2] | Need prior phase notes, markers, deploy evidence, and remaining work | 1 |
| read-by | [agent:bob-cli-ph.7.1.land--1][3] | Re-read every child phase and its completion notes for final landing verification | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.7.1.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.7.1.4/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.7.1.land.md

<!-- sase:referenced-by:end -->
