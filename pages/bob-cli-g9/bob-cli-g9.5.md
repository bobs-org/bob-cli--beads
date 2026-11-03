# Bead: bob-cli-g9.5 — One rung-aware decay card

[Bead Pages](../README.md) / [bob-cli-g9](README.md) / bob-cli-g9.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.32.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.32.linker.w0.md) · **Assignee:** `bob-cli-g9.5` · **Size:** medium
**Created:** 2026-11-02 15:55:43 EST · **Closed:** 2026-11-02 20:48:39 EST
**Plan:** [202611/task\_decay\_ladder.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_decay_ladder.md)

## Description

nav-card: generalize the decay card to every rung: Enter steps exactly one rung (WIP to Next, Next to Ready, Ready to the entry level, P-level to the next, P4 rolls again) while bypassing the roll streak, Alt+F stays and resets the count, each answer is one composed and undoable write with its Rotten Log entry, batches skip at-limit lane targets, and the card capability rises to 3.

## Notes

[2026-11-03T01:48:16Z · bob-cli-g9.5--1] PROPOSED FOLLOW-UP: Sync task-status-cycler successor vectors — plugins copy still at pre-71907dab (SA31/SA32 as v1.1 UI), bob-cli canonical moved them to non-UI capture unlink; test fails identically on clean base.

[2026-11-03T01:48:24Z · bob-cli-g9.5--1] PROPOSED FOLLOW-UP: Pre-existing bob-plugins failures reproduce on clean base — schedule-work-log future-Pending Blocked ([?] vs [/]), freshness-namespace reload event, note-ready startup storm (1 vs 2), relation-index layout-ready timeout, sheet-sequence-dom missing Chromium, plus flaky Live Preview perf and reduced-motion CSS under full-suite load (both pass in isolation).

[2026-11-03T01:48:39Z · bob-cli-g9.5--1] nav-card verified: fixed footer D/X drop-alias regression in 051 snapshot, updated 3 stale expectations (P0 reason now kept 3x in Ready, Next keep subtitle includes decay-card notice, decision-card footers use D/X). Decay suites green: planner 27, roll-decay 60, decision-card 26, handlers 30, keep 13, rotten-keep 35, rotten-log 7, review-journal 9, task-card-view 92. npm build, docs:inventory:check, docs:check (447 passed) and just docs-check pass. bob plugins sync -F deployed navigation-hotkeys 2.73.0. epic-symbols clean. Remaining full-suite reds (vectors sync, schedule-Blocked, namespace reload, startup storm, relation-index, Chromium, flaky perf/motion) reproduce identically on clean base and are recorded as follow-ups.

## Dependencies

- **Depends on:** [bob-cli-g9.4](bob-cli-g9.4.md) ✓ · ⧖ 2026-11-02
- **Blocks:** [bob-cli-g9.6](bob-cli-g9.6.md) ✓ · ⧖ 2026-11-02
- **Blocks:** [bob-cli-g9.7](bob-cli-g9.7.md) ✓ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-g9.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-g9.5.md) | [bob-cli-g9.5](bob-cli-g9.5.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`817ba7d`](https://github.com/bobs-org/bob-cli/commit/817ba7dda9579138fb93a1690177fb5ac20c1bcb) | docs(freshness): add freshness and projects notes for nav-card decay work | [bob-cli-g9.5](bob-cli-g9.5.md) | 2026-11-02 20:51:09 EST |
| bob-plugins | [`bob-plugins@6464cad`](https://github.com/bobs-org/bob-plugins/commit/6464cad318ea87033106b674c4b5019b5131b93a) | fix(nav-hotkeys): restore D/X drop alias and rung-aware decay contract | [bob-cli-g9.5](bob-cli-g9.5.md) | 2026-11-02 20:51:43 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-g9.5--1][1] | Need remaining work and notes before fixing test failures | 5 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-g9.5.md

<!-- sase:referenced-by:end -->
