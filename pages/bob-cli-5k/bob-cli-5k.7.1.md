# Bead: bob-cli-5k.7.1 — Migrate zorg-era reading records into the reference library

[Bead Pages](../README.md) / [bob-cli-5k.7](bob-cli-5k.7.md) / bob-cli-5k.7.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-5k.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-5k.7.md) · **Assignee:** `bob-cli-5k.7.1.land`
**Created:** 2026-10-07 16:17:59 EDT · **Closed:** 2026-10-07 20:44:24 EDT
**Plan:** [202610/zorg\_ref\_migration.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/zorg_ref_migration.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/zorg_ref_migration.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/zorg_ref_migration.md

<!-- sase:links:end -->

## Description

`bob ref migrate-zorg` moves every unindexed zorg-era reading record (424 on 2026-10-07) into legacy reference notes under `ref/zorg/<hub>/`. It runs as a dry-run-first, idempotent vault write: one sync-sandwiched commit that a single `git revert` undoes. Book chapters fold into their book's note. On athena, `bob ref doctor` then reports `coverage: ok`, `bob ref find` / `bob ref list` return the migrated records, the JSON `coverage.scope` caveat no longer claims that zorg history is invisible, and bob-cli-4x is closed.

## Notes

[2026-10-08T00:44:24Z · bob-cli-5k.7.1.land] Verified all four phases closed with notes, and master 74c2afc matches them.

record-model (db6bcdb): ZorgRecord parser, source_id/source_blocks provenance, and legacy_chapter_statuses book state. Shared-block pairs in ~/bob stay distinct (prj_gbd ^z-250425-0f owns bidder_declarations_prd and cs_bidder_dec; zettlr_ref ^z-250326-0r owns zettlr_wtf_is_zettelkasten and zettlr_projects).

planner (937722b): dry-run `bob ref migrate-zorg` in the Library group (find, list, migrate-zorg, show). About is one line: "Migrate zorg-era records to ref/zorg/; dry run unless --write". tests/cli/help.rs rejects a wrapped Library about.

writer (74c2afc): --write takes bob_sync.lock, pre-syncs, re-plans, refuses existing targets and a dirty ref/zorg, writes create-new files, verifies through the index and coverage and deletes its own files on failure, then one scoped commit and a post-sync. Coverage::scope_text and docs/ref.md match the plan's replacement caveat. The rollback runbook is in docs/ref.md, with a pointer in docs/vault-git-sync.md.

live-run re-checked with installed bob against ~/bob: doctor coverage ok (935 notes; diagnostics still only the two pre-existing ref/ai opaque_url rows). migrate-zorg reports 0 to migrate and already migrated 706 (282+424). find http://go/cs-bidder-dec and https://vimhelp.org/quickfix.txt.html are in_library. list -s legacy -t books shows 11 notes: the 7 started chapter-books, Clean Arch and System For Writing finished, War Of Art unknown, plus Alfreds Piano Course 1 queued. work_clean_ref is legacy_status book with ref_type zorg, so it is outside -t books. clean_arch_ref renders ## Chapters. Vault HEAD is 36bf2172f018095d8cb2330810cf6588ed02ed95, 322 files all under ref/zorg/**, worktree clean.

Integration: four commits landed after this epic started and are not its own (39915c5 return links, cc9bd5f just check, 577866d Tasks JS sandbox, 73f9cc4 LaTeX packages). None duplicate or conflict with migrate-zorg. highlights_ref still has both the LaTeX doctor rows and the migrate-zorg dispatch. No code change.

Follow-ups declined, not filed:
- bob-cli-5k.7.1.2 note #1 (papers 49 vs the plan table's 48): live-run accepted it. The table sums to 323, not 322. The planner follows rule 3.3 (first file:: value). The notes are already migrated.
- bob-cli-5k.7.1.2 note #2 (Library abouts shortened to one line): the writer kept that constraint, and tests/cli/help.rs locks it. Restoring the longer section 3.9 sentence would wrap.
- Writer notes on cargo not rebuilding and git revert pruning an empty ref/ are operational, not PROPOSED FOLLOW-UP entries. Athena's ref/ holds real notes, so the live revert does not remove it.

No --epic-symbol entries. Closed bob-cli-4x with the doctor row, migration sha, and rollback command. Writer and live-run already reported just check green on this same master; this landing did not change bob-cli source, so just check was not re-run.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-5k.7.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5k.7.1.land/README.md) | [bob-cli-5k.7.1](bob-cli-5k.7.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli--plans | [`bob-cli--plans@174c6dc`](https://github.com/bobs-org/bob-cli--plans/commit/174c6dcc44e513ee3d74660e68cfa31281ea2e62) | docs(plans): mark zorg\_ref\_migration done | [bob-cli-5k.7.1](bob-cli-5k.7.1.md) | 2026-10-07 20:46:45 EDT |
