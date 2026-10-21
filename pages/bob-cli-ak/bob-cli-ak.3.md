# Bead: bob-cli-ak.3 — Recurrence marks in Tasks query results

[Bead Pages](../README.md) / [bob-cli-ak](README.md) / bob-cli-ak.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.28.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.28.linker.w0.md) · **Assignee:** `bob-cli-ak.3` · **Size:** small
**Created:** 2026-10-21 08:49:59 EDT · **Closed:** 2026-10-21 10:21:43 EDT
**Plan:** [202610/gtd\_checklist\_glyphs\_and\_recurrence\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/gtd_checklist_glyphs_and_recurrence_marks.md)

## Description

recurrence-tasks: extend the full-mode Tasks frame pass to `span.task-recurring`, draw the loop glyph in short mode with CSS, add `hide recurrence rule` to the vault's blocked.md RECURRING query, and add the RT conformance vectors.

## Notes

[2026-10-21T14:21:31Z · bob-cli-ak.3--1] PROPOSED FOLLOW-UP: npm test has 6 pre-existing failures that reproduce identically on the clean base tree (stashed 267-task-recurring work, ran the 4 files: 62 pass / 6 fail) — 4x test-ledger-tools-unblocked-glyph.cjs (Live Preview glyph after unblocked link), Keep-counts saturation in test-navigation-decision-card-handlers.cjs, Depends-On forward-promotion in test-navigation-hotkeys-forward-promotion.cjs; plus 1 load-sensitive flake (stage-ranker 18ms vs 16ms budget under full suite, passes 23/23 in isolation on the dirty tree)

[2026-10-21T14:21:43Z · bob-cli-ak.3--1] RT1-RT6 green (82/82 across date-marks-tasks, recurrence-marks, date-marks suites); full-mode span.task-recurring host with loop mark + checklist guard, short-mode CSS loop, toggle-off cover, docs/date-marks.md contract+vectors, manifest 1.63.0, bob plugins sync verified byte-identical in vault, blocked.md hide recurrence rule committed (b9507dc1); npm/build:check/docs:check/just docs-gen/docs-check all pass; 6 npm failures reproduce identically on clean base (recorded as PROPOSED FOLLOW-UP), 1 perf flake passes in isolation; epic-symbols clean

## Dependencies

- **Depends on:** [bob-cli-ak.2](bob-cli-ak.2.md) ✓ · ⧖ 2026-10-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ak.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ak.3.md) | [bob-cli-ak.3](bob-cli-ak.3.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8e81f3c`](https://github.com/bobs-org/bob-cli/commit/8e81f3ccd61f20cd35ac9ed569f1ba4c474dac36) | docs(date-marks): specify Tasks recurrence-mark host, guard, and RT vectors | [bob-cli-ak.3](bob-cli-ak.3.md) | 2026-10-21 10:23:14 EDT |
| bob-plugins | [`bob-plugins@3e014b9`](https://github.com/bobs-org/bob-plugins/commit/3e014b9942f3de917c671a0f5b927f32927b4d84) | feat(ledger-tools): render recurrence marks in Tasks query results | [bob-cli-ak.3](bob-cli-ak.3.md) | 2026-10-21 10:24:21 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ak.3][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ak.3.md

<!-- sase:referenced-by:end -->
