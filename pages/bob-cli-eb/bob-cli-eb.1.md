# Bead: bob-cli-eb.1 — Table-layout Lua pass with prose-table records

[Bead Pages](../README.md) / [bob-cli-eb](README.md) / bob-cli-eb.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2u.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2u.linker.w0.md) · **Assignee:** `bob-cli-eb.1` · **Size:** medium
**Created:** 2026-10-29 20:03:06 EDT · **Closed:** 2026-10-29 20:54:54 EDT
**Plan:** [202610/ref\_table\_layout\_for\_highlights.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_table_layout_for_highlights.md)

## Description

records-filter: build the embedded table_layout.lua pass (classification, override precedence, complex-table guard, row-record layout, JSON report) plus its TeX macros and Rust embedding module, tested by running pandoc on the filter directly.

## Notes

[2026-10-30T00:54:29Z · bob-cli-eb.1] PROPOSED FOLLOW-UP: skipped decisions memory strand for prose-tables-print-as-records — epic auto-decision decision_record=no forbids editing decisions; land agent should file a memory task to add a strand recording that prose tables print as records

[2026-10-30T00:54:54Z · bob-cli-eb.1] Embedded table_layout.lua/.tex/.rs: 22/22 pandoc-gated tests pass (classification 12-word boundary, overrides, complex-table guard, native fidelity, lead-in, lists/quotes, nested, xelatex PDF). improve_grid is a named no-op. Clippy gates clean for the new module. header_packages_are_all_declared includes TABLE_LAYOUT_HEADER_INCLUDES. epic-symbols: no leftovers. Skipped decisions strand recorded as PROPOSED FOLLOW-UP.

[2026-10-30T01:45:48Z · bob-cli-eb.1--1] PROPOSED FOLLOW-UP: native::capture_related::tests::archive_closed_window_respects_mtime fails on clean master (also bob-cli-e6.6, bob-cli-e8.3) — stale done/ note with [completion:: 2026-10-01] still matches as closed_duplicate (days_ago=19) despite 40-day mtime; window follows pinned today vs real SystemTime::now()

## Dependencies

- **Blocks:** [bob-cli-eb.2](bob-cli-eb.2.md) ✓ · ⧖ 2026-10-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-eb.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-eb.1.md) | [bob-cli-eb.1](bob-cli-eb.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b47617d`](https://github.com/bobs-org/bob-cli/commit/b47617dc9e066a9bb0c53ddf724f01f81b7007f0) | feat(ref): embed table-layout Lua pass for prose-table records | [bob-cli-eb.1](bob-cli-eb.1.md) | 2026-10-29 21:53:00 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-eb.1--1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-eb.1.md

<!-- sase:referenced-by:end -->
