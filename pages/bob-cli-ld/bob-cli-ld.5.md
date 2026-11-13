# Bead: bob-cli-ld.5 — Highlights snapshot renders the projects catalog

[Bead Pages](../README.md) / [bob-cli-ld](README.md) / bob-cli-ld.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1c6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1c6.md) · **Assignee:** `bob-cli-ld.5` · **Size:** small
**Created:** 2026-11-13 10:58:46 EST · **Closed:** 2026-11-13 12:22:39 EST
**Plan:** [202611/subprojects\_catalog\_section.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/subprojects_catalog_section.md)

## Description

highlights-snapshot: render [!projects] in Highlights PDFs with state chips, omitting the Closed group, while legacy notes keep their masthead row.

## Notes

[2026-11-13T17:22:14Z · bob-cli-ld.5] PROPOSED FOLLOW-UP: just lint/check is red on the clean base tree from five deny-level clippy diagnostics in src/native/gmail/unarchive.rs (clippy::needless_borrow at 283 twice, 313, 330; clippy::useless_conversion at 464), introduced by commit 2ddfc944 for bob-cli-kx.3.1.3 — already tracked on bob-cli-kx / bob-cli-kx.3.1.4; this phase did not touch that file.

[2026-11-13T17:22:39Z · bob-cli-ld.5] Highlights PDFs render [!projects] as a linked callout of open rows with scheduled/blocked/needs ^prj chips, omit the Closed group (and the heading when nothing remains), and keep the legacy Sub-projects masthead on marker-only notes. Verified by cargo test --lib native::highlights_ref::note_snapshot (178 passed), including catalog-only, legacy-only, and all-closed goldens. No leftover --epic-symbol entries. just lint is red on the clean base tree (gmail/unarchive.rs clippy); recorded as PROPOSED FOLLOW-UP citing bob-cli-kx.

## Dependencies

- **Blocks:** [bob-cli-ld.10](bob-cli-ld.10.md) ◐ · ⧖ 2026-11-13
- **Depends on:** [bob-cli-ld.2](bob-cli-ld.2.md) ✓ · ⧖ 2026-11-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ld.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ld.5/README.md) | [bob-cli-ld.5](bob-cli-ld.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a225953`](https://github.com/bobs-org/bob-cli/commit/a2259538b9785597bb0572c01e6a145c0fce463f) | feat(highlights): render the projects catalog in note snapshots | [bob-cli-ld.5](bob-cli-ld.5.md) | 2026-11-13 12:24:30 EST |
