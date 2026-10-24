# Bead: bob-cli-bd.4 — Sectioned rendering and identity

[Bead Pages](../README.md) / [bob-cli-bd](README.md) / bob-cli-bd.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2d.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2d.linker.w0.md) · **Assignee:** `bob-cli-bd.4` · **Size:** large
**Created:** 2026-10-24 07:59:21 EDT · **Closed:** 2026-10-24 10:41:53 EDT
**Plan:** [202610/ref\_note\_annotation\_sections.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_note_annotation_sections.md)

## Description

render: restructure render_sidecar_highlights into collect-then-assemble, emit the sectioned layout with consumed tags, apply the both-sides @-insensitive identity keys, route declaration #task lines to the s- block, and prove byte-identical output for undeclared notes plus ID stability through tag toggles.

## Notes

[2026-10-24T14:00:37Z · bob-cli-bd.4] PROPOSED FOLLOW-UP: record the annotation-sections design as decisions:annotation-sections-are-name-keyed-folds — epic decision_record=no declined this memory change; leave the note untouched and defer triage to the epic land agent.

[2026-10-24T14:00:44Z · bob-cli-bd.4] PROPOSED FOLLOW-UP: add the Annotation Section glossary term — epic glossary_term=no declined this memory change; leave glossary:annotation-section untouched and defer triage to the epic land agent.

[2026-10-24T14:41:30Z · bob-cli-bd.4] PROPOSED FOLLOW-UP: tests/cli/highlights/continuations.rs continuation_scan_reports_dangling_marker fails identically on clean base 453b07e7 and with render changes (expected "continuation_dangling: Page 11 (no earlier text highlight)", got "Page 1"); continuation_scan_tucks_two_pages_and_is_idempotent also fails identically on both trees (tucked group renders as Page 1 instead of Pages 11-12). Repro: cargo test --test cli -- highlights::continuations::continuation_scan_reports_dangling_marker highlights::continuations::continuation_scan_tucks_two_pages_and_is_idempotent. No known tracking bead; does not block phase close per plan.

[2026-10-24T14:41:53Z · bob-cli-bd.4] Implemented sectioned rendering with stable IDs: collect-then-assemble DisplayBlocks in sidecar_render.rs, SectionPlan after folds, H3 section cards with [!summary|section] captions (tag count pages), beautified descriptions with image-note resolution via s- block ID, H4 page captions resetting per H3, Other highlights only when ungrouped, Removed last; rejected declarations render as literal \# heading ordinary notes, accepted declarations produce no h-IDs; both-sides @-insensitive identity via section_match_key (note/comment keys, deduped effective comments, annotation_block_id, absorbed matching), declaration orders mapped to s-<slug> in both ID maps, RenderedHighlights.sections + section_diagnostics populated. Verified: 11 new sections_render tests pass; 676 highlights_ref lib tests pass unchanged; just docs-check passed; just check green except 2 pre-existing cli continuations failures reproducing identically on base 453b07e7 (recorded as PROPOSED FOLLOW-UP); vault scan dry-run base vs current exact match (520 pdfs, 503 unchanged, 17 updated, notes[] identical, read-only, timestamps ignored). Limitations: indistinguishable twin quotes fall back to order-based ID association (documented, no stability promise); diagnostics/report wiring left to bd.6; no vault mutations.

## Dependencies

- **Depends on:** [bob-cli-bd.2](bob-cli-bd.2.md) ✓ · ⧖ 2026-10-24
- **Depends on:** [bob-cli-bd.3](bob-cli-bd.3.md) ✓ · ⧖ 2026-10-24
- **Blocks:** [bob-cli-bd.6](bob-cli-bd.6.md) ✓ · ⧖ 2026-10-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-bd.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-bd.4.md) | [bob-cli-bd.4](bob-cli-bd.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`9398c5b`](https://github.com/bobs-org/bob-cli/commit/9398c5bbcca27fce050e67e029bd5a02bc60fbeb) | feat(highlights): sectioned annotation rendering with stable IDs | [bob-cli-bd.4](bob-cli-bd.4.md) | 2026-10-24 10:43:22 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.2][1] | Identify the existing owner and task evidence for clean-base just check failures | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-an.6.6.6.5.6.5.2/README.md

<!-- sase:referenced-by:end -->
