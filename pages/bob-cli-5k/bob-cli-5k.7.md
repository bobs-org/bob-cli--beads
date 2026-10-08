# Bead: bob-cli-5k.7 — Migrate zorg-era reading records into the reference library

[Bead Pages](../README.md) / [bob-cli-5k](README.md) / bob-cli-5k.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0y2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0y2.md) · **Assignee:** `bob-cli-5k.7` · **Size:** xlarge
**Created:** 2026-10-07 14:38:42 EDT · **Closed:** 2026-10-07 20:44:24 EDT
**Plan:** [202610/close\_top\_ten\_impact\_beads.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/close_top_ten_impact_beads.md)

## Description

ref-migration: settle the migration design with Bryan, author and drive a nested epic that moves the ~424 unindexed zorg-era reading records into `ref/` through a dry-run-first, idempotent, reversible vault write, and close bob-cli-4x once `bob ref doctor` coverage confirms it.

## Notes

[2026-10-07T20:04:12Z · bob-cli-5k.7] INVENTORY (athena, 2026-10-07, live ~/bob, release bob; script mirrors coverage.rs rules): bob ref doctor coverage = 424 unindexed records across 37 files (work_ref 75, nvim_ref 69, clean_arch 37, dev_ref 27, prj_yserve 18, ad_tech_book 17, soft_arch_hard_parts 16, zorg_ref 14, prj_gbd 12, ...). By status: READ 135, REVIEW_FLEETING_NOTES 96, COLLECT_FLEETING_NOTES 92, UNREAD 57, REVIEW_LIT_NOTES 17, ABANDONED 16, BOOK 11. By kind: 160 public-URL readings; 137 internal (128 http://go/..., 2 google3, rest work hubs); 101 LID:: chapter/section records inside 9 book notes (clean_arch, ad_tech_book, soft_arch_hard_parts, system_for_writing, balance_coupling, cat_theory_for_devs, how_to_read_a_book, outlive, think_fast_and_slow), each of which also holds one BOOK record; 26 with placeholder/non-http url:: (-, NONE, None, MULTIPLE, [[wikilink]], ~/path). Every record has an owner ^z- block. Collisions: 0 normalized-URL hits vs existing ref/ notes; 0 ID vs ref/ basename hits; 0 top-level ID shared across files; 2 lowercase block-id collisions within one file (prj_gbd ^z-250425-0F/0f, zettlr_ref ^z-250326-0R/0r) so (source_path, source_block) is not unique; 4 bobdoto_ref records share one page URL (different sections). go/ hosts pass clip_url::validate_and_clean (no opaque_url). Precedent sase-4b.1 (vault a478dd9) wrote ref/ai/<hub>/<ID>.md with status legacy + legacy_status + url + source_note/block/id/path/line_start/line_end and an escaped Original Record block, and left hub lines untouched.

[2026-10-08T00:45:12Z · bob-cli-5k.7.1.land] Landing re-check after bob-cli-5k.7.1 closed. The phase's work is done: Bryan settled the design in plan:202610/zorg_ref_migration.md, the nested epic's four phases landed on master 74c2afc, and the live vault write is ~/bob 36bf2172f018095d8cb2330810cf6588ed02ed95 (424 records, 322 notes, all under ref/zorg/**). Installed bob ref doctor reports coverage ok. bob ref migrate-zorg reports 0 to migrate. bob-cli-4x is closed with that sha and the git-revert rollback. This phase was closed by the nested landing as delegated work landed; this note is the verification.

## Dependencies

- **Depends on:** [bob-cli-5k.3](bob-cli-5k.3.md) ✓ · ⧖ 2026-10-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-5k.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-5k.7.md) | [bob-cli-5k.7](bob-cli-5k.7.md) | 0 |
