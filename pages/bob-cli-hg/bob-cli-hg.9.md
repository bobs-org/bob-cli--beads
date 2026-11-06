# Bead: bob-cli-hg.9 — bob gmail search, peek, and list --remote

[Bead Pages](../README.md) / [bob-cli-hg](README.md) / bob-cli-hg.9

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.cn](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.cn.md) · **Assignee:** `bob-cli-hg.9` · **Size:** medium
**Created:** 2026-11-05 12:37:50 EST · **Closed:** 2026-11-06 07:48:53 EST
**Plan:** [202611/bob\_gmail.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bob_gmail.md)

## Description

gmail-search-peek: bounded thread search for pickers, a read-only metadata peek with a small private cache for live previews, and remote new-message counts for saved threads.

## Notes

[2026-11-06T12:40:07Z · bob-cli-hg.9] PROPOSED FOLLOW-UP: refresh the docs README contract table snapshot — just docs-check failed at test_readme_table_matches_original_contract_index_snapshot (expected fedc20a..., current 96a429d5...; 446 passed, 1 skipped). docs/README.md and tools/docs/tests/test_contracts.py are unchanged from HEAD; bob-cli-hl.5.1.5 already records the same clean-master drift.

[2026-11-06T12:48:31Z · bob-cli-hg.9] PROPOSED FOLLOW-UP: resolve the pre-existing clipboard catalog overlap — native::catalog::tests::public_leaves_are_entries_or_excluded still fails because unchanged clipboard is in ENTRIES and EXCLUDED; tracked by bob-cli-hp and confirmed on clean base in bob-cli-hg.4 / bob-cli-hg.6.1 evidence.

[2026-11-06T12:48:53Z · bob-cli-hg.9] Implemented bounded Gmail search, metadata-only peek with private body-free cache, and list --remote counts; added catalog/completion entries, fake-gog coverage, and docs. Verified cargo check --bin bob; Gmail integration tests 5/5 and gmail_shell 24/24; cargo fmt --all -- --check and git diff --check; just docs-gen. Catalog tests passed 10/11, with public_leaves_are_entries_or_excluded failing only on the pre-existing clipboard entry/exclusion overlap tracked by bob-cli-hp and reproduced on clean base (noted above). just docs-check reached its Python contract test and failed only the known README snapshot drift, already tracked by bob-cli-hl.5. epic-symbols reported no leftovers.

## Dependencies

- **Blocks:** [bob-cli-hg.10](bob-cli-hg.10.md) ◐ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hg.11](bob-cli-hg.11.md) ◐ · ⧖ 2026-11-05
- **Depends on:** [bob-cli-hg.6](bob-cli-hg.6.md) ✓ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-hg.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.9/README.md) | [bob-cli-hg.9](bob-cli-hg.9.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e1e8006`](https://github.com/bobs-org/bob-cli/commit/e1e800602be1e46b1d46adb46aedd768dca74391) | feat(gmail): add search, peek, and remote counts | [bob-cli-hg.9](bob-cli-hg.9.md) | 2026-11-06 07:50:22 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:research.5s.grk][1] | Need remaining Gmail phase user-facing scopes for the guide | 1 |
| read-by | [agent:research.5s.mus][2] | gmail user guide research | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.5s.grk/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.5s.mus/README.md

<!-- sase:referenced-by:end -->
