# Bead: bob-cli-ir.9 — bob records init plus show and movie types

[Bead Pages](../README.md) / [bob-cli-ir](README.md) / bob-cli-ir.9

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1a0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1a0.md) · **Assignee:** `bob-cli-ir.9` · **Size:** medium
**Created:** 2026-11-08 11:06:12 EST · **Closed:** 2026-11-09 08:25:49 EST
**Plan:** [202611/record\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/record_notes.md)

## Description

records-media-types: add bob records init to scaffold a type's folder, type note, collection note, and Base, then ship the show (tv/) and movie (movies/) types in config and the vault.

## Notes

[2026-11-09T12:41:02Z · bob-cli-ir.9] Verified: bob records init TYPE [-d] [-p PARENT] scaffolds type note, collection note, and starter Base; never creates empty <dir>/; existing files kept. show (tv/) and movie (movies/) schemas in chezmoi config.yml. Vault: init show kept tv.md; init movie -p fun created movie.md, movies.md, movies.base. Tuned tv.base/movies.base (To Watch, Watching for TV, Watched grouped by verdict, All). types.json watched_on=date year=number. Seeded 32 to_watch records (23 shows, 9 movies). Created shows: Lioness, Landman, Designated Survivor (recommended_by=eric); WandLa, Murderbot, Side Quest, Silo (service=Apple TV+); Star Trek: Lower Decks, Jury Duty, Upload, Reservation Dogs, Georgie & Mandy's First Marriage, South Park, The Boys; Happy's Place, Lost, Manifest (recommended_by=nona); The Paper, Attack on Titan; Abbott Elementary, Foundation, Invincible; The Studio (note w/ Seth Rogan). Created movies: Mrs Doubtfire, The Messenger, Equilibrium, Romantic Comedy, F1, Thunderbolts (Disney Plus), Sucker Punch, 9, Batman: Nightfall. Skipped: Special Ops: Lioness (dup of Lioness), Download new shows! container, Invincible comes out on 2026-03-18! (dup), Download S4 of Hacks (#fun not #plex), love.md non-movie tasks. Task lines untouched. bob records check show/movie 0 errors. epic-symbols clean. docs-gen/docs-check done. glossary:capture left for bob-cli-ir.13.

[2026-11-09T12:57:55Z · bob-cli-ir.9--1] Repaired just check: records init TYPE completion kind (RecordType) plus --parent VaultNote; catalog document_shape count 84→85. Unit tests document_shape, every_value_arg_has_a_decision, and every_table_entry_matches_the_tree pass. epic-symbols still clean.

[2026-11-09T13:25:49Z · bob-cli-ir.9--2] Closed by explicit `sase stitch create -B close` after create_commit landed 262f3cfc ("feat(records): add records init CLI to scaffold type notes and Bases"). The commit author requested bead completion after verifying the bead scope. Reopen with `sase bead open bob-cli-ir.9` if more work remains.

## Dependencies

- **Blocks:** [bob-cli-ir.13](bob-cli-ir.13.md) ✓ · ⧖ 2026-11-08
- **Depends on:** [bob-cli-ir.4](bob-cli-ir.4.md) ✓ · ⧖ 2026-11-08
- **Depends on:** [bob-cli-ir.7](bob-cli-ir.7.md) ✓ · ⧖ 2026-11-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ir.9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ir.9.md) | [bob-cli-ir.9](bob-cli-ir.9.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`262f3cf`](https://github.com/bobs-org/bob-cli/commit/262f3cfcbf594449a247bb5925e10ba7ca89fb34) | feat(records): add records init CLI to scaffold type notes and Bases | [bob-cli-ir.9](bob-cli-ir.9.md) | 2026-11-09 08:25:16 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ir.9--2][1] | Need the phase scope, notes, and whether work already landed after just check passed | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ir.9.md

<!-- sase:referenced-by:end -->
