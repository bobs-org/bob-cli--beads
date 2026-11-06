# Bead: bob-cli-hg.6.1.4 — List saved mail offline and diagnose identity health

[Bead Pages](../README.md) / [bob-cli-hg.6.1](bob-cli-hg.6.1.md) / bob-cli-hg.6.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-hg.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-hg.6.md) · **Assignee:** `bob-cli-hg.6.1.4` · **Size:** medium
**Created:** 2026-11-05 23:47:36 EST · **Closed:** 2026-11-06 05:06:27 EST
**Plan:** [202611/gmail\_save\_list.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_save_list.md)

## Description

list-diagnostics: implement real bare/explicit list with pagination and backlinks, body-free JSON, decoder and duplicate diagnostics, catalog/help/docs updates, and the remaining cross-layer acceptance checks. Leave remote refresh and link-failure footer population to the existing outer epic phases.

## Notes

[2026-11-06T09:43:09Z · bob-cli-hg.6.1.4] PROPOSED FOLLOW-UP: tools/docs tests/test_contracts.py::test_readme_table_matches_original_contract_index_snapshot fails identically on clean HEAD (README contract-table snapshot stale); refresh the snapshot or the table outside this phase.

[2026-11-06T10:06:02Z · bob-cli-hg.6.1.4] PROPOSED FOLLOW-UP: three gate failures reproduce identically on clean HEAD and are unrelated to list-diagnostics — catalog public_leaves clipboard in both lists, completion kinds stale clipboard:count duplicate, cli root_help snapshot missing the gmail line (stale since the gmail noun landed).

[2026-11-06T10:06:27Z · bob-cli-hg.6.1.4] Implemented list-diagnostics: real offline bare/explicit gmail list with updated-desc sort and path tiebreak, 20-row default with -a for all, body-free table/JSON, one-pass Markdown-aware backlink counts (aliases, heading/block targets; code/frontmatter/self excluded), duplicate identities as diagnostics plus skipped_malformed counts, gmail_urls decoder census and gmail_duplicates warn rows in doctor (run even when sign-in fails), gmail-list catalog read entry, docs/gmail.md List/Try-it/doctor updates with regenerated CLI reference. Verified: cargo fmt clean, just lint gate passes, lib gmail 165 tests green, gmail_shell 24/24 green, full workspace suite green except 4 failures that reproduce identically on clean HEAD (recorded as PROPOSED FOLLOW-UP notes: docs README contract snapshot, catalog clipboard both-lists, completion clipboard:count duplicate, cli root_help gmail line).

## Dependencies

- **Depends on:** [bob-cli-hg.6.1.3](bob-cli-hg.6.1.3.md) ✓ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-hg.6.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.6.1.4/README.md) | [bob-cli-hg.6.1.4](bob-cli-hg.6.1.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`fcc4efa`](https://github.com/bobs-org/bob-cli/commit/fcc4efa51f6f4cca2f0c5f7dd1d1cab2a4ffff24) | feat(gmail): list saved mail offline and diagnose identity health | [bob-cli-hg.6.1.4](bob-cli-hg.6.1.4.md) | 2026-11-06 05:07:42 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hg.6.1.4][1] | Need phase scope and design | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.6.1.4/README.md

<!-- sase:referenced-by:end -->
