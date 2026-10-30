# Bead: bob-cli-eb.2 — Wire the table pass into both pandoc chains, config, and docs

[Bead Pages](../README.md) / [bob-cli-eb](README.md) / bob-cli-eb.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2u.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2u.linker.w0.md) · **Assignee:** `bob-cli-eb.2` · **Size:** medium
**Created:** 2026-10-29 20:03:06 EDT · **Closed:** 2026-10-29 23:36:39 EDT
**Plan:** [202610/ref\_table\_layout\_for\_highlights.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_table_layout_for_highlights.md)

## Description

pandoc-wiring: add highlights.table_layout and highlights.table_prose_words, run the pass first in the Markdown and note-snapshot chains, print the tables summary line and warnings, cover the return-link and code-catalog contracts end to end, and document the feature in help and docs.

## Notes

[2026-10-30T03:36:28Z · bob-cli-eb.2] PROPOSED FOLLOW-UP: Add decisions strand prose-tables-print-as-records (skipped per epic decision_record=no; needs human review of the auto plan first)

[2026-10-30T03:36:39Z · bob-cli-eb.2] Wired table-layout pass first on both pandoc chains with highlights.table_layout/table_prose_words config, tables: line + kept-grid warnings, e2e return-link/catalog tests on both routes, Tables docs + config rows + help sentence. Verified: cargo fmt clean, just lint clean, full workspace suite green (3968 lib + 2472 cli + all integration, 0 failed); snapshot xelatex render asserts skip here (missing titlesec/lastpage/xurl) but the snapshot pandoc chain was verified manually (records + 1 longtable + 2/1/1 report + paired anchors), and the Markdown full-PDF render ran green via a mutool-backed pdftotext shim.

## Dependencies

- **Depends on:** [bob-cli-eb.1](bob-cli-eb.1.md) ✓ · ⧖ 2026-10-29
- **Blocks:** [bob-cli-eb.3](bob-cli-eb.3.md) ✓ · ⧖ 2026-10-29
- **Blocks:** [bob-cli-eb.4](bob-cli-eb.4.md) ✓ · ⧖ 2026-10-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-eb.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-eb.2/README.md) | [bob-cli-eb.2](bob-cli-eb.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`7d765b8`](https://github.com/bobs-org/bob-cli/commit/7d765b80e89549700ea4f88a0633c4181f0bb338) | feat(highlights): add configurable table layout for reference renders | [bob-cli-eb.2](bob-cli-eb.2.md) | 2026-10-29 23:38:21 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-eb.2][1] | phase scope | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-eb.2/README.md

<!-- sase:referenced-by:end -->
