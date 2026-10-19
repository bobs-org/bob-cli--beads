# Bead: bob-cli-9r.4 — Today marks in Live Preview with toggle and jump

[Bead Pages](../README.md) / [bob-cli-9r](README.md) / bob-cli-9r.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.11r](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.11r.md) · **Assignee:** `bob-cli-9r.4` · **Size:** medium
**Created:** 2026-10-19 09:47:17 EDT · **Closed:** 2026-10-19 10:44:08 EDT
**Plan:** [202610/today\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/today_marks.md)

## Description

live_preview: add the src/275-plugin-today-marks.js mixin (ViewPlugin decorations, refresh fan-out, session toggle, the Mod+click and keyboard jump to the Task Link) and lifecycle wiring. Run the TM vectors against Live Preview, then bump, build, test, and sync.

## Notes

[2026-10-19T14:41:50Z · bob-cli-9r.4] PROPOSED FOLLOW-UP: Record decisions:today-mark-shows-ledger-today in the decisions web if reopened — the final plan choice for this phase was no, so no memory note was edited.

[2026-10-19T14:41:54Z · bob-cli-9r.4] PROPOSED FOLLOW-UP: Repair clean-base npm test failures tracked by bob-cli-6v, bob-cli-6w, and bob-cli-7i — this run reproduced four unblocked-glyph failures, the Keep-count notice failure, and the forward-conversion reverse failure unchanged on the clean base tree.

[2026-10-19T14:44:08Z · bob-cli-9r.4] Implemented and synced Live Preview Today marks, toggle, and daily Task Link jumps; build and all 25 Today mark tests pass. Full npm test has six unrelated failures that reproduce identically on clean base and are recorded as follow-ups; epic-symbol check found none.

## Dependencies

- **Depends on:** [bob-cli-9r.1](bob-cli-9r.1.md) ✓ · ⧖ 2026-10-19
- **Depends on:** [bob-cli-9r.3](bob-cli-9r.3.md) ✓ · ⧖ 2026-10-19
- **Blocks:** [bob-cli-9r.5](bob-cli-9r.5.md) ✓ · ⧖ 2026-10-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-9r.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9r.4/README.md) | [bob-cli-9r.4](bob-cli-9r.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@e4c71bc`](https://github.com/bobs-org/bob-plugins/commit/e4c71bc4a548bbe1e10261b3aa489100bae87283) | feat(ledger-tools): add Today marks to Live Preview | [bob-cli-9r.4](bob-cli-9r.4.md) | 2026-10-19 10:46:08 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-9r.4][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9r.4/README.md

<!-- sase:referenced-by:end -->
