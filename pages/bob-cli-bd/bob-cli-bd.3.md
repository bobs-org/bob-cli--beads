# Bead: bob-cli-bd.3 — Sectioned managed-region parser

[Bead Pages](../README.md) / [bob-cli-bd](README.md) / bob-cli-bd.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2d.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2d.linker.w0.md) · **Assignee:** `bob-cli-bd.3` · **Size:** medium
**Created:** 2026-10-24 07:59:21 EDT · **Closed:** 2026-10-24 08:21:16 EDT
**Plan:** [202610/ref\_note\_annotation\_sections.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_note_annotation_sections.md)

## Description

region: teach parse_managed_region to read sectioned regions (section H3 + summary|section card + ^s- line, #### page captions, Other highlights) into RegionParse.sections and RegionBlock.section, leaving every unsectioned region parsed exactly as today.

## Notes

[2026-10-24T12:15:09Z · bob-cli-bd.3] PROPOSED FOLLOW-UP: skipped memory change — decisions:annotation-sections-are-name-keyed-folds was auto-declined; record the annotation-sections design as a decisions strand when the epic lands if Bryan wants it.

[2026-10-24T12:15:16Z · bob-cli-bd.3] PROPOSED FOLLOW-UP: skipped memory change — glossary:annotation-section was auto-declined; add an Annotation Section glossary term when the epic lands if Bryan wants it.

[2026-10-24T12:21:16Z · bob-cli-bd.3] parse_managed_region reads sectioned regions (H3 + [!summary|section] card + ^s- line, #### captions, Other highlights, Removed ^s- tombstones) into RegionParse.sections/removed_sections and RegionBlock.section; unsectioned regions parse as today; cards never count as annotations; generated_block_ids stays h-only; region unit tests plus just check (fmt, clippy, full cargo test) passed; no --epic-symbol leftovers.

## Dependencies

- **Blocks:** [bob-cli-bd.4](bob-cli-bd.4.md) ◐ · ⧖ 2026-10-24
- **Blocks:** [bob-cli-bd.5](bob-cli-bd.5.md) ◐ · ⧖ 2026-10-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-bd.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bd.3/README.md) | [bob-cli-bd.3](bob-cli-bd.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b7645d1`](https://github.com/bobs-org/bob-cli/commit/b7645d17ba1a98caf43b8607e863e16c03bb5fc1) | feat(highlights-ref): parse sectioned managed regions | [bob-cli-bd.3](bob-cli-bd.3.md) | 2026-10-24 08:22:20 EDT |
