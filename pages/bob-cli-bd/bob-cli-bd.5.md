# Bead: bob-cli-bd.5 — Sections in bob ref show

[Bead Pages](../README.md) / [bob-cli-bd](README.md) / bob-cli-bd.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2d.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2d.linker.w0.md) · **Assignee:** `bob-cli-bd.5` · **Size:** medium
**Created:** 2026-10-24 07:59:21 EDT · **Closed:** 2026-10-24 08:50:14 EDT
**Plan:** [202610/ref\_note\_annotation\_sections.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_note_annotation_sections.md)

## Description

show: add the additive sections list and per-annotation section key to bob ref show JSON, and grouped human and Markdown output, with -c/-N semantics and docs/ref.md updates.

## Notes

[2026-10-24T12:49:55Z · bob-cli-bd.5] PROPOSED FOLLOW-UP: record decisions:annotation-sections-are-name-keyed-folds — epic decision_record was no, so the annotation-sections design was not written as a decisions strand

[2026-10-24T12:49:55Z · bob-cli-bd.5] PROPOSED FOLLOW-UP: add glossary:annotation-section — epic glossary_term was no, so the Annotation Section glossary term was not added

[2026-10-24T12:50:14Z · bob-cli-bd.5] Verified bob ref show JSON adds sections (id/title/tag/block_id/link/count, optional description/pages/images) and annotations[].section; -N omits sections; -c keeps the full sections list while human/Markdown print a header only when a member is kept. Grouped human (magenta ▍, bold title, dim caption/description) and Markdown (#### Title, italic caption, > description, Other highlights) match the contract; unsectioned rows stay omitted/byte-identical. TASKS uses dim § Title for s- block ids. cargo fmt --check, cargo clippy --all-targets --all-features, cargo test --lib native::ref_library::show::tests, cargo test --test cli -- ref_library::show, and just docs-check passed. No leftover --epic-symbol entries.

## Dependencies

- **Depends on:** [bob-cli-bd.3](bob-cli-bd.3.md) ✓ · ⧖ 2026-10-24
- **Blocks:** [bob-cli-bd.7](bob-cli-bd.7.md) ✓ · ⧖ 2026-10-24
- **Blocks:** [bob-cli-bd.8](bob-cli-bd.8.md) ✓ · ⧖ 2026-10-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-bd.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bd.5/README.md) | [bob-cli-bd.5](bob-cli-bd.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`94591ea`](https://github.com/bobs-org/bob-cli/commit/94591ea66d48c89fba305344c40d0df5bfceecc6) | feat(ref): group bob ref show output by annotation sections | [bob-cli-bd.5](bob-cli-bd.5.md) | 2026-10-24 08:51:41 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.2][1] | Identify the existing owner and task evidence for clean-base just check failures | 1 |
| read-by | [agent:bob-cli-bd.5][2] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-an.6.6.6.5.6.5.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bd.5/README.md

<!-- sase:referenced-by:end -->
