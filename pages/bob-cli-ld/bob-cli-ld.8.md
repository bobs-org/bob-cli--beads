# Bead: bob-cli-ld.8 — Capture writes the parent catalog row at birth

[Bead Pages](../README.md) / [bob-cli-ld](README.md) / bob-cli-ld.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1c6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1c6.md) · **Assignee:** `bob-cli-ld.8` · **Size:** medium
**Created:** 2026-11-13 10:58:46 EST · **Closed:** 2026-11-13 16:11:40 EST
**Plan:** [202611/subprojects\_catalog\_section.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/subprojects_catalog_section.md)

## Description

catalog-at-birth: project-note captures stage the parent's catalog row in the same all-or-nothing batch, refusing a damaged parent catalog.

## Notes

[2026-11-13T20:47:21Z · bob-cli-ld.8] PROPOSED FOLLOW-UP: just docs-check lint budget still over cap on unmodified pages docs/reference/json-outputs.md (6025), bob-ledger-tools.md (6115), and bob-navigation-hotkeys.md (6019) — tracked by bob-cli-il and bob-cli-jz; reproduces on files this phase did not edit

[2026-11-13T21:07:47Z · bob-cli-ld.8--1] PROPOSED FOLLOW-UP: just check fails native::gcal::cli::tests::sync_args_read_last_n_days_aliases_and_default_to_none on clean HEAD 7cd57603 — tracked by bob-cli-l2; left ["tomorrow"] vs right ["today", "tomorrow"] at src/native/gcal/cli.rs:1032

[2026-11-13T21:11:40Z · bob-cli-ld.8--1] Project-note create and offer stage the parent ## Projects catalog in the same all-or-nothing batch; a leftover Sub-projects line migrates; a damaged [!projects] region refuses with projects_catalog_damaged and writes nothing; dry-run names both files. Human output prints wrote/updated (or would write/would update) plus the catalog hint; JSON adds optional project_note.parent_catalog {path, action}. glossary:project-note-capture now says the same batch lists the note in the parent catalog. Verified: cargo fmt, 87 project-note CLI tests, 1 np-move fixture test, sase bead epic-symbols (no leftovers). just check still fails native::gcal::cli::tests::sync_args_read_last_n_days_aliases_and_default_to_none on clean HEAD (bob-cli-l2).

## Dependencies

- **Blocks:** [bob-cli-ld.10](bob-cli-ld.10.md) ◐ · ⧖ 2026-11-13
- **Depends on:** [bob-cli-ld.7](bob-cli-ld.7.md) ✓ · ⧖ 2026-11-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ld.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ld.8.md) | [bob-cli-ld.8](bob-cli-ld.8.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f9b6159`](https://github.com/bobs-org/bob-cli/commit/f9b6159334dff607c681f90382693a0fa36c723a) | feat(capture): list new project notes in the parent Projects catalog at birth | [bob-cli-ld.8](bob-cli-ld.8.md) | 2026-11-13 16:13:44 EST |
