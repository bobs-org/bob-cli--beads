# Bead: bob-cli-9r.3 — Today mark pure core, widget, and styles

[Bead Pages](../README.md) / [bob-cli-9r](README.md) / bob-cli-9r.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.11r](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.11r.md) · **Assignee:** `bob-cli-9r.3` · **Size:** medium
**Created:** 2026-10-19 09:47:17 EDT · **Closed:** 2026-10-19 10:17:38 EDT
**Plan:** [202610/today\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/today_marks.md)

## Description

mark_core: add src/143-today-marks.js (line candidate, insert offset, duplicate ids, session text, tooltip, listener-free element, TodayMarkWidget) plus the styles.css block and a new test suite for the pure vectors.

## Notes

[2026-10-19T14:17:26Z · bob-cli-9r.3] PROPOSED FOLLOW-UP: Record decisions:today-mark-shows-ledger-today memory strand (epic chose memory_today_mark_record=no, so mark_core wrote none)

[2026-10-19T14:17:30Z · bob-cli-9r.3] PROPOSED FOLLOW-UP: Full npm test has 6 pre-existing failures on the clean base tree, not just the 4 known bob-cli-6v unblocked-glyph ones — also keeps saturation and Depends-On conversion

[2026-10-19T14:17:38Z · bob-cli-9r.3] mark_core landed: src/143-today-marks.js pure core + widget, styles.css block, 21-test suite all green, build:check + validate clean, bumped to 1.58.3, plugins synced; full suite shows only the 6 base-identical pre-existing failures

## Dependencies

- **Depends on:** [bob-cli-9r.2](bob-cli-9r.2.md) ✓ · ⧖ 2026-10-19
- **Blocks:** [bob-cli-9r.4](bob-cli-9r.4.md) ✓ · ⧖ 2026-10-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-9r.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9r.3/README.md) | [bob-cli-9r.3](bob-cli-9r.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@66a9597`](https://github.com/bobs-org/bob-plugins/commit/66a95978033fc0837943ad2cdec5255b91588493) | feat(ledger-tools): add today-marks fragment with element, widget and styles | [bob-cli-9r.3](bob-cli-9r.3.md) | 2026-10-19 10:19:36 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-9r.3][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9r.3/README.md

<!-- sase:referenced-by:end -->
