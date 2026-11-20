# Bead: bob-cli-o6.3 — Album \`title:\` key, H1-less album create, and \`bob albums tidy\`

[Bead Pages](../README.md) / [bob-cli-o6](README.md) / bob-cli-o6.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1eh](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1eh.md) · **Assignee:** `bob-cli-o6.3` · **Size:** large
**Created:** 2026-11-20 11:49:16 EST · **Closed:** 2026-11-20 12:47:17 EST
**Plan:** [202611/property\_card\_title\_block.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/property_card_title_block.md)

## Description

album-title-cli: in bob-cli, make frontmatter `title:` the first title source for album notes in every reader, make bob albums create write `title:` and no H1, and add bob albums tidy (dry-run by default) that backfills `title:` from the H1 and removes the now-redundant H1 under record-tidy keep rules, with registry, completion, docs, and no-churn sync tests. No live-vault apply in this phase.

## Notes

[2026-11-20T17:46:35Z · bob-cli-o6.3] LIVE DRY RUN (obsidian-proof evidence): after just install on athena, `bob albums tidy -f json` (no -a) against ~/bob exited 0 with ok=true, dry_run=true, counts {scanned: 6, changed: 6, title_added: 6, h1_removed: 6, h1_kept: 0}; kept_h1=[]; warnings=[]; io_errors=[]; vault HEAD unchanged. Planned titles: eat.md 'Restaurants', movies.md 'Movies', podcasts.md 'Podcasts', sase_blog_zettel.md 'SASE Blog Zettel', subscriptions.md 'Subscriptions', tv.md 'TV'. Each diff inserts title: after type and removes the H1 plus its blank line, leaving ---, blank, intro.

[2026-11-20T17:46:40Z · bob-cli-o6.3] PROPOSED FOLLOW-UP: records tidy member about omits H1 removal — src/runner.rs RECORDS_MEMBERS 'tidy' about says 'Remove empty `## Notes` sections from Record Notes' while the clap about (and docs) also remove redundant H1s; the bob records group long help likewise says only 'tidy removes empty ## Notes sections'. Align both with the clap about.

[2026-11-20T17:46:45Z · bob-cli-o6.3] PROPOSED FOLLOW-UP: mixed-version album titles — an older bob derives album titles only from the H1, so (a) after the obsidian-proof apply removes H1s, and (b) for any album created by this bob (born with title: and no H1), an older bob running `bob albums sync` on another host (apollo, mac) rewrites walk lines and [!albums] catalog rows to the humanized stem. Upgrade every host that runs album sync before the live apply and before creating albums elsewhere; consider whether obsidian-proof should check host versions first.

[2026-11-20T17:46:50Z · bob-cli-o6.3] PROPOSED FOLLOW-UP: docs/records.md misplaced paragraph — the albums sync JSON paragraph ('JSON uses schema version 1. `albums[]` repeats the list/check entry shape…', now line 254) sits at the end of the records-tidy section instead of under 'Syncing records indexes'. Move it back under the sync section.

[2026-11-20T17:46:55Z · bob-cli-o6.3] PROPOSED FOLLOW-UP: BOM-prefixed album notes are not albums — projects::parse_frontmatter requires line 1 to be exactly '---', so an album file that starts with a UTF-8 BOM is never registered and bob albums tidy/sync/list never see it. The tidy planner itself preserves BOM bytes (unit-tested), but album discovery would need to strip the BOM first. Pre-existing; no live album has a BOM today.

[2026-11-20T17:47:17Z · bob-cli-o6.3] Album readers take frontmatter title first (FrontmatterTitle on AlbumDeclaration; album_title_invalid warning on unusable values). bob albums create writes title: after type and no H1, with a parse-back refusal. New bob albums tidy [STEM] [-a] [-b] [-f] (dry run by default) inserts title from the current reader title and strips the redundant H1 via strip_redundant_h1, reporting kept H1s (incl. fenced) and refusing invalid titles or damaged frontmatter; registered in native, runner, completion (AlbumStem), and catalog (Excluded one-time migration). Gates: just fmt, just check (exit 0, all test binaries ok), just docs-gen, just docs-check all pass; vault-format.md trimmed to stay under its 6000-word cap. No-churn integration test (tests/cli/albums_tidy.rs): real sync, tidy -a, re-sync is a no-op; records, [!records] region, body.md catalog, and list titles byte-identical. just install on athena done. Live read-only dry run: scanned 6, changed 6, title_added 6, h1_removed 6, h1_kept 0, no warnings, HEAD unchanged; no -a against the live vault.

## Dependencies

- **Blocks:** [bob-cli-o6.6](bob-cli-o6.6.md) ◐ · ⧖ 2026-11-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-o6.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-o6.3.md) | [bob-cli-o6.3](bob-cli-o6.3.md) | 0 |
