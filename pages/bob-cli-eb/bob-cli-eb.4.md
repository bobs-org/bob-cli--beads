# Bead: bob-cli-eb.4 — Records and grid cleanup on the web-clip print route

[Bead Pages](../README.md) / [bob-cli-eb](README.md) / bob-cli-eb.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2u.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2u.linker.w0.md) · **Assignee:** `bob-cli-eb.4` · **Size:** medium
**Created:** 2026-10-29 20:03:07 EDT · **Closed:** 2026-10-30 00:53:01 EDT
**Plan:** [202610/ref\_table\_layout\_for\_highlights.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_table_layout_for_highlights.md)

## Description

web-clip: carry the table settings in the adapter request, rewrite prose tables into record markup on the print DOM only, clean up reader.css grids, report counts back to bob, and add a tables fixture to the adapter self-test.

## Notes

[2026-10-30T04:27:52Z · bob-cli-eb.4--2] PROPOSED FOLLOW-UP: Consider adding a decisions memory strand that prose tables print as records; skipped here because this phase decision sets decision_record=false.

[2026-10-30T04:38:29Z · bob-cli-eb.4--3] PROPOSED FOLLOW-UP: Fix the clean-base CLI test `ref_library::today::today_matches_unnamed_capture_and_named_capture_remembers_theme` — reproduced on base 7d765b80 with Pomodoros text mismatch (the unnamed `READ` entry and its reference link are placed differently); it also fails in this phase checkout, so this phase did not introduce it.

[2026-10-30T04:53:01Z · bob-cli-eb.4--4] web-clip adapter self-test ok; docs-check all gates passed; just all has single pre-existing failure ref_library::today::today_matches_unnamed_capture_and_named_capture_remembers_theme identical on clean base 7d765b80 (2483 passed/1 failed both trees), recorded as PROPOSED FOLLOW-UP; epic-symbols clean

## Dependencies

- **Depends on:** [bob-cli-eb.2](bob-cli-eb.2.md) ✓ · ⧖ 2026-10-29
- **Blocks:** [bob-cli-eb.6](bob-cli-eb.6.md) ✓ · ⧖ 2026-10-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-eb.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-eb.4.md) | [bob-cli-eb.4](bob-cli-eb.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a984ec5`](https://github.com/bobs-org/bob-cli/commit/a984ec5755138c678842aa2fd39ce6c38c8863e7) | feat(web-clip): records and grid cleanup on print route | [bob-cli-eb.4](bob-cli-eb.4.md) | 2026-10-30 00:59:41 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-eb.4--4][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-eb.4.md

<!-- sase:referenced-by:end -->
