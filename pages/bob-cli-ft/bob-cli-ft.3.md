# Bead: bob-cli-ft.3 — Checkbox rendering in Live Preview and reading view, CSS, toggle, tooltips

[Bead Pages](../README.md) / [bob-cli-ft](README.md) / bob-cli-ft.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.16w](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.16w.md) · **Assignee:** `bob-cli-ft.3` · **Size:** large
**Created:** 2026-11-02 06:28:10 EST · **Closed:** 2026-11-02 11:44:56 EST
**Plan:** [202611/blocked\_reason\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/blocked_reason_marks.md)

## Description

editor_marks: render the marks on Blocked checkboxes in Live Preview, reading view, embeds, hover previews, and Dataview TASK views. Covers the gated CSS families and tokens, glyph masks and the corner pip, the session toggle, hover tooltips, invalidation, api.blockMarks.render, a contrast test, and a real-Obsidian e2e harness with light and dark screenshots.

## Notes

[2026-11-02T16:45:27Z · bob-cli-ft.3.1.land--1] Verified child epic bob-cli-ft.3.1 and its landing repair complete the editor_marks scope; just check passed (monitor rp04x2zzmm7r, exit 0). Focused reading 28/28; live xvfb e2e 114/114; report file:explicit:f826b23ed46ccb980f3496b6. Manifest 1.90.1. Vault left at clean 1.90.0 from canonical bob-plugins 806ba69 (sync --no-pull refused: forcing would regress day-strip). Host commits after this turn.

Dispositions:
- et, f7, eh, ff, f8: corroborated existing tasks; independent evidence file:explicit:55a612058c1373e9ca6880b1; no new task.
- Reduced-motion: declined; focused motion tests pass 2/2.
- Decisions remain own_first, chevron, quiet, memory_decision_record=no. Stored Markdown stays [?].
- Live Dataview of this Obsidian build does not emit origin; harness injects proven origin on BM4; adapter recovers from Tasks cache; unprovable rows stay unmarked.
- BM23 is a controlled clock (dateMarksToday + refreshDateMarksForRollover), not a midnight observation.

Leave outer epic bob-cli-ft open.

## Dependencies

- **Depends on:** [bob-cli-ft.2](bob-cli-ft.2.md) ✓ · ⧖ 2026-11-02
- **Blocks:** [bob-cli-ft.4](bob-cli-ft.4.md) ✓ · ⧖ 2026-11-02
- **Blocks:** [bob-cli-ft.7](bob-cli-ft.7.md) ✓ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ft.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ft.3.md) | [bob-cli-ft.3](bob-cli-ft.3.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ft.3.1.1][1] | Need epic DECISIONS and scope | 1 |
| read-by | [agent:bob-cli-ft.3.1.3][2] | Need rendering scope and final epic decisions | 2 |
| read-by | [agent:bob-cli-ft.3.1.4][3] | Need rendering scope and final epic decisions | 1 |
| read-by | [agent:bob-cli-ft.3.1.land--1][4] | Verify parent phase status after child close and reread before parent closeout | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ft.3.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ft.3.1.3/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ft.3.1.4/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ft.3.1.land.md

<!-- sase:referenced-by:end -->
