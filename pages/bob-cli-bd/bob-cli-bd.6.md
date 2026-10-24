# Bead: bob-cli-bd.6 — Section stubs, diagnostics, and route hints

[Bead Pages](../README.md) / [bob-cli-bd](README.md) / bob-cli-bd.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2d.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2d.linker.w0.md) · **Assignee:** `bob-cli-bd.6` · **Size:** medium
**Created:** 2026-10-24 07:59:21 EDT · **Closed:** 2026-10-24 11:33:13 EDT
**Plan:** [202610/ref\_note\_annotation\_sections.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_note_annotation_sections.md)

## Description

edges: add redirect stubs for a published declaring sticky and for a vanished but linked section, the dry-run/concise/JSON section diagnostics, the missing-route hint, and the tag-on-task diagnostic.

## Notes

[2026-10-24T15:32:33Z · bob-cli-bd.6] PROPOSED FOLLOW-UP: Pre-existing `completion::kinds::every_value_arg_has_a_decision` lib failure (themes rename:old/new lack kinds decisions, from the themes-rename commit) reproduces on the clean base; needs a fix in the themes area, out of scope for edges.

[2026-10-24T15:32:43Z · bob-cli-bd.6] PROPOSED FOLLOW-UP: Pre-existing cli failures reproduce on the clean base: highlights::continuations scan tests x2, capture perf-gate timing, and flaky capture_text named-start tests (pass in isolation); all unrelated to section edges.

[2026-10-24T15:32:49Z · bob-cli-bd.6] PROPOSED FOLLOW-UP: Skipped memory decision_record per epic plan (auto): consider recording decisions:annotation-sections-are-name-keyed-folds when the epic lands.

[2026-10-24T15:32:56Z · bob-cli-bd.6] PROPOSED FOLLOW-UP: Skipped memory glossary_term per epic plan (auto): consider adding glossary:annotation-section when the epic lands.

[2026-10-24T15:33:13Z · bob-cli-bd.6] Edges done: declaring-sticky redirect stubs (appear/linked, persist/unlinked, disappear), removed-section stubs (appear/linked, persist/stubbed, disappear/redeclare), dry-run section lines for all 9 diagnostics, concise N sections/N unknown counts, scan JSON sections/section_tags_unknown with omit-when-zero, missing-route section hint with still-routes precedence. 11 new section_edges tests + 2 scan_json serde tests pass; full highlights_ref suite 692 green; fmt+clippy gates pass; 6 full-suite failures all reproduce identically on clean base (recorded as follow-ups). No Cargo.toml/CHANGELOG touches.

## Dependencies

- **Depends on:** [bob-cli-bd.4](bob-cli-bd.4.md) ✓ · ⧖ 2026-10-24
- **Blocks:** [bob-cli-bd.7](bob-cli-bd.7.md) ✓ · ⧖ 2026-10-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-bd.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bd.6/README.md) | [bob-cli-bd.6](bob-cli-bd.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`be18197`](https://github.com/bobs-org/bob-cli/commit/be1819783e6285882bb05d66e38d5d6b0a139056) | feat(highlights): section stubs, diagnostics, and route hints | [bob-cli-bd.6](bob-cli-bd.6.md) | 2026-10-24 11:34:25 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-bd.6][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bd.6/README.md

<!-- sase:referenced-by:end -->
