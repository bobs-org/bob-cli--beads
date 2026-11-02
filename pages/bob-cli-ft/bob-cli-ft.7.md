# Bead: bob-cli-ft.7 — Task Card reason header and teaching digit (bob-navigation-hotkeys)

[Bead Pages](../README.md) / [bob-cli-ft](README.md) / bob-cli-ft.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.16w](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.16w.md) · **Assignee:** `bob-cli-ft.7` · **Size:** medium
**Created:** 2026-11-02 06:28:11 EST · **Closed:** 2026-11-02 11:57:59 EST
**Plan:** [202611/blocked\_reason\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/blocked_reason_marks.md)

## Description

task_card: the Task Card's BLOCKED lane chip becomes the block mark plus every reason in After / Until / Via words (the touch and mobile path). The P1–P4 strip shows the hollow digit box beside each level's bars. Both go through api.blockMarks v1 and fall back to today's look when the api is missing.

## Notes

[2026-11-02T16:57:48Z · bob-cli-ft.7] PROPOSED FOLLOW-UP: Full bob-plugins npm test has 5 failures that reproduce identically on the clean base tree (no task_card regression): test-ledger-tools-note-ready.cjs reload-event key-set test, test-ledger-tools-freshness-namespace.cjs forced-check feedback test, test-ledger-tools-keep-inbox.cjs startup-storm linearity test, test-ledger-tools-relation-index.cjs startup-replay test, test-navigation-hotkeys-schedule-work-log.cjs Pending-future-schedule Work Log test

[2026-11-02T16:57:59Z · bob-cli-ft.7] Task Card BLOCKED chip renders the api.blockMarks v1 miniature with After/Until/Via reason list for single Blocked targets; P1-P4 strip shows decorative hollow teaching digits; counted batches and missing api fall back to today's look. Verified: 92/92 task-card view tests, 21/21 task-card model tests, 252/252 across 9 task-card+block-marks files, build:check, validate 8/8, docs:check, docs:gen, bob plugins sync deployed. 5 unrelated full-suite failures reproduce on clean base, recorded as follow-up.

## Dependencies

- **Depends on:** [bob-cli-ft.3](bob-cli-ft.3.md) ✓ · ⧖ 2026-11-02
- **Blocks:** [bob-cli-ft.8](bob-cli-ft.8.md) ✓ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ft.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ft.7/README.md) | [bob-cli-ft.7](bob-cli-ft.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@31852e6`](https://github.com/bobs-org/bob-plugins/commit/31852e695d7fda4dbd3ead9c58f19eec5268b23d) | feat(nav-hotkeys): show blocked-reason mark and reasons on the Task Card | [bob-cli-ft.7](bob-cli-ft.7.md) | 2026-11-02 12:02:07 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ft.7][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ft.7/README.md

<!-- sase:referenced-by:end -->
