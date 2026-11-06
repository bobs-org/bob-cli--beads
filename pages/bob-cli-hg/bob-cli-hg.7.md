# Bead: bob-cli-hg.7 — bob gmail link — swap Gmail URLs for labelled links, and backfill

[Bead Pages](../README.md) / [bob-cli-hg](README.md) / bob-cli-hg.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.cn](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.cn.md) · **Assignee:** `bob-cli-hg.7` · **Size:** medium
**Created:** 2026-11-05 12:37:49 EST · **Closed:** 2026-11-06 08:31:05 EST
**Plan:** [202611/bob\_gmail.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bob_gmail.md)

## Description

gmail-link: find Gmail URLs in named notes or the whole vault, save each confirmed thread, replace exactly those URL tokens with labelled wikilinks under the lock, remember dead links, preview with a diff, and report waiting links in list.

## Notes

[2026-11-06T13:30:22Z · bob-cli-hg.7] PROPOSED FOLLOW-UP: catalog clipboard dual-listing fails just check on clean tree (native::catalog::tests::public_leaves_are_entries_or_excluded and native::completion::kinds::tests::every_table_entry_matches_the_tree both report ["clipboard"] / duplicate clipboard:count); reproduced identically with changes stashed

[2026-11-06T13:30:35Z · bob-cli-hg.7] PROPOSED FOLLOW-UP: root help snapshot predates the gmail group (help::root_help_matches_sectioned_short_and_long_snapshots fails on clean tree; stored snapshot lacks the gmail line that bob gmail has printed since gmail-shell)

[2026-11-06T13:30:42Z · bob-cli-hg.7] PROPOSED FOLLOW-UP: docs contract-table snapshot hash is stale on clean tree (tools/docs/tests/test_contracts.py::test_readme_table_matches_original_contract_index_snapshot fails with changes stashed)

[2026-11-06T13:31:05Z · bob-cli-hg.7] bob gmail link lands: named-note and -a backfill scan, token-exact swaps under one lock with save-path resolution, dead links journaled by digest and skipped, awaiting_sign_in marker, -d unified diff, waiting/gone list footer. Verified: 10 new link unit tests + 167 lib gmail tests pass; 10 new link integration tests + full 34 gmail_shell pass; cli catalog 8 pass; full clippy gate 0 errors; fmt clean; docs-gen regenerated with docs-check showing only the pre-existing readme-snapshot failure. 4 clean-tree failures recorded as PROPOSED FOLLOW-UPs (clipboard dual-listing x2 tests, root-help snapshot, readme snapshot).

## Dependencies

- **Depends on:** [bob-cli-hg.6](bob-cli-hg.6.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hg.8](bob-cli-hg.8.md) ◐ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-hg.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.7/README.md) | [bob-cli-hg.7](bob-cli-hg.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f075147`](https://github.com/bobs-org/bob-cli/commit/f075147f4bb928427a7b21501e863b3c99051b5e) | feat(gmail): swap Gmail URLs for labelled links, and backfill | [bob-cli-hg.7](bob-cli-hg.7.md) | 2026-11-06 09:57:47 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hg.7][1] | check notes and remaining work | 2 |
| read-by | [agent:research.5s.cld][2] | Check phase status and any design refinements for the Gmail user guide | 1 |
| read-by | [agent:research.5s.grk][3] | Need remaining Gmail phase user-facing scopes for the guide | 1 |
| read-by | [agent:research.5s.mus][4] | gmail user guide research | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.7/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.5s.cld/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.5s.grk/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.5s.mus/README.md

<!-- sase:referenced-by:end -->
