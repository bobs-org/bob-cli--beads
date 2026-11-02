# Bead: bob-cli-fe.7 — Ctrl+S splits the selected Pomodoro (bob-plugins)

[Bead Pages](../README.md) / [bob-cli-fe](README.md) / bob-cli-fe.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.c4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.c4.md) · **Assignee:** `bob-cli-fe.7` · **Size:** medium
**Created:** 2026-11-01 16:00:43 EST · **Closed:** 2026-11-02 06:14:35 EST
**Plan:** [202611/merged\_pomodoros.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/merged_pomodoros.md)

## Description

obsidian-ctrl-s: add the planSplit mirror, a contextual Ctrl+S dispatch, a palette command, the two-type auto split, and the multi-select split picker with refusals, docs, and tests.

## Notes

[2026-11-02T11:14:23Z · bob-cli-fe.7] PROPOSED FOLLOW-UP: 5 pre-existing bob-plugins failures reproduce identically on clean base (no split changes applied) — test-command-mode-sheet-sequence-dom Chromium missing, test-ledger-tools-freshness-namespace reload-event, test-ledger-tools-note-ready startup storm, test-ledger-tools-relation-index startup replay, test-navigation-hotkeys-schedule-work-log future-scheduling Pending Blocked; full suite 4947 pass / same 5 fail with and without this phase

[2026-11-02T11:14:35Z · bob-cli-fe.7] Ctrl+S split delivered in bob-plugins: api.themes.planSplit mirror passes all 14 shared split vectors; planPomodoroTypeSplit NAV planner moves Task Link subtrees into name-ordered entries; capture-phase Ctrl+S dispatch with save-file fallback, split-pomodoro-by-type palette command, and Tab-marked multi-select picker; docs/API prose, manifest 2.67.0/1.84.0, new harness suite 9/9; full suite 4947 pass with only the 5 pre-existing base failures (noted as follow-up); bob plugins sync not forced — vault holds bob-cli_21 uncommitted deployment

## Dependencies

- **Blocks:** [bob-cli-fe.10](bob-cli-fe.10.md) ✓ · ⧖ 2026-11-01
- **Depends on:** [bob-cli-fe.6](bob-cli-fe.6.md) ✓ · ⧖ 2026-11-01
- **Blocks:** [bob-cli-fe.8](bob-cli-fe.8.md) ✓ · ⧖ 2026-11-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-fe.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fe.7/README.md) | [bob-cli-fe.7](bob-cli-fe.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@3bab3c0`](https://github.com/bobs-org/bob-plugins/commit/3bab3c0345f589455c7a9b81f009e51535e7967e) | feat(bob-plugins): Ctrl+S splits the selected Pomodoro by type | [bob-cli-fe.7](bob-cli-fe.7.md) | 2026-11-02 06:16:16 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-fe.7][1] | Need full bead including notes JSON | 3 |
| read-by | [agent:bob-cli-fe.8][2] | Check whether the reproduced baseline plugin test failure is already tracked | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fe.7/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fe.8/README.md

<!-- sase:referenced-by:end -->
