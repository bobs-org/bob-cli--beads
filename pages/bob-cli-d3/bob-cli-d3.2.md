# Bead: bob-cli-d3.2 — Single web articles save source.md and a catalog

[Bead Pages](../README.md) / [bob-cli-d3](README.md) / bob-cli-d3.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.ao](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.ao.md) · **Assignee:** `bob-cli-d3.2` · **Size:** medium
**Created:** 2026-10-27 11:21:28 EDT · **Closed:** 2026-10-27 12:38:03 EDT
**Plan:** [202610/web\_ref\_saved\_sources.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/web_ref_saved_sources.md)

## Description

web-article-store: read Chrome catalog /Dests, convert the source view to GFM, catalog it with the existing filters, map anchor and annotation pages, and write the web_article store and pointer on every single-article create path, with tests and docs.

## Notes

[2026-10-27T16:37:53Z · bob-cli-d3.2] PROPOSED FOLLOW-UP: highlights::store_gaps::store_snapshot_create_records_note_snapshot_route fails on this host with missing titlesec.sty (xelatex); reproduces identically on the clean base tree, unrelated to web-article-store

[2026-10-27T16:38:03Z · bob-cli-d3.2] web_article store ships: pdf_dests reads Chrome catalog /Dests (tree wins), record_source_catalog + orphan-adoption accept web_article/web_collection with gfm reader, new web_source.rs converts source view to GFM/catalogs/maps anchor+annotation pages/persists store on all single-article branches (incl -H/reread/--audio/--listen, -k birth adoption via digest). Verified: 4 new integration tests (store+route+pointer, code json exact tabbed bytes with anchor pages, --source round-trip, links json annotation pages, -o none, no-view none, -k scan adoption), lib 3747 green, cli 2297/2298 (1 pre-existing titlesec.sty env failure, base-identical, filed as follow-up), clippy/fmt/docs-gen/docs-check green. ref.md unchanged: every saved-source/code/link statement already route-generic (verified). No decision record per epic DECISIONS.

## Dependencies

- **Depends on:** [bob-cli-d3.1](bob-cli-d3.1.md) ✓ · ⧖ 2026-10-27
- **Blocks:** [bob-cli-d3.3](bob-cli-d3.3.md) ◐ · ⧖ 2026-10-27
- **Blocks:** [bob-cli-d3.5](bob-cli-d3.5.md) ◐ · ⧖ 2026-10-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-d3.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-d3.2/README.md) | [bob-cli-d3.2](bob-cli-d3.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4fda80b`](https://github.com/bobs-org/bob-cli/commit/4fda80b13d65e59383e847073622145f3c72acd8) | feat(web-ref): single web articles save source.md and a catalog | [bob-cli-d3.2](bob-cli-d3.2.md) | 2026-10-27 12:41:16 EDT |
