# Bead: bob-cli-lr.2 — Marked titles in the daily note

[Bead Pages](../README.md) / [bob-cli-lr](README.md) / bob-cli-lr.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.4q.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.4q.linker.w1.md) · **Assignee:** `bob-cli-lr.2` · **Size:** medium
**Created:** 2026-11-15 12:24:27 EST · **Closed:** 2026-11-15 13:58:29 EST
**Plan:** [202611/gcal\_calendar\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gcal_calendar_marks.md)

## Description

marked-rows: render the mark at the front of the Google-owned title span through one shared helper used for rendering and journal span hashes. New rows are born marked; untouched rows follow mark changes in place; hand-edited titles are kept and reported once; block ids and probes stay on the bare title.

## Notes

[2026-11-15T18:57:53Z · bob-cli-lr.2] PROPOSED FOLLOW-UP: docs-check lint fails on clean base too — docs/reference/configuration.md is 6009 words vs the 6000-word reference/ cap (likely pushed over by lr.1 config-docs addition); needs a trim or cap bump

[2026-11-15T18:58:29Z · bob-cli-lr.2] marked-rows done: row_title helper in render.rs fronts the mark on the Google-owned title span; mark flows SyncedCalendar->PlannedOccurrence->render with journal span hashing the marked span while block ids, needs_meet_type probe, @route stripping stay bare; reset/replaced/text-match paths reuse render_occurrence so marked rows never look edited. Verified: 2 new render unit tests, 10 new gcal_sync integration tests (Ava born-marked exact bullet + idempotent rerun, multi-day qualifier after mark, timed Event Task with bare block id dawn-patrol, @body strip to bare title, mark-change in-place update, primary byte-identical no-churn, hand-edit kept once, distinct instance ids), full gcal_sync 110 pass, all other gcal suites pass, fmt+clippy clean. Docs: gcal.md marked example + Calendar mark ownership row, vault-format mark grammar. docs-check lint fails identically on clean base (configuration.md 6009/6000 words, pre-existing) — recorded as PROPOSED FOLLOW-UP.

## Dependencies

- **Depends on:** [bob-cli-lr.1](bob-cli-lr.1.md) ✓ · ⧖ 2026-11-15
- **Blocks:** [bob-cli-lr.4](bob-cli-lr.4.md) ◐ · ⧖ 2026-11-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-lr.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-lr.2/README.md) | [bob-cli-lr.2](bob-cli-lr.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`5acbc8a`](https://github.com/bobs-org/bob-cli/commit/5acbc8a8f8f6f08913b682b3b48bc4d227f24426) | feat(gcal): render calendar marks at the front of Google-owned title spans | [bob-cli-lr.2](bob-cli-lr.2.md) | 2026-11-15 14:01:57 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-lr.2][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-lr.2/README.md

<!-- sase:referenced-by:end -->
