# Bead: bob-cli-hg.6.1.3 — Save and refresh mail notes under the vault lock

[Bead Pages](../README.md) / [bob-cli-hg.6.1](bob-cli-hg.6.1.md) / bob-cli-hg.6.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-hg.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-hg.6.md) · **Assignee:** `bob-cli-hg.6.1.3` · **Size:** medium
**Created:** 2026-11-05 23:47:35 EST · **Closed:** 2026-11-06 04:10:40 EST
**Plan:** [202611/gmail\_save\_list.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_save_list.md)

## Description

save-transaction: implement the save CLI and reusable staged save API, writer gate, parent-at-birth, hubs, agent warning, lock/re-read/retry, atomic text writes and safe image promotion, exact-path commit, and post-commit journals. Add save catalog coverage, docs, and adversarial transaction tests.

## Notes

[2026-11-06T08:49:32Z · bob-cli-hg.6.1.3] PROPOSED FOLLOW-UP: Reconcile clean-base gate failures. `just check` passed fmt and Clippy, then failed only the duplicate clipboard tests native::catalog::tests::public_leaves_are_entries_or_excluded and native::completion::kinds::tests::every_table_entry_matches_the_tree (already tracked by bob-cli-hp), plus help::root_help_matches_sectioned_short_and_long_snapshots because unchanged root fixtures omit Gmail (same clean-base failure recorded in bob-cli-hg.6.1.1 note #1; no task bead found). The newly introduced every_value_arg_has_a_decision failure for gmail save:input was fixed here and its focused rerun passed. `just docs-check` passed all gates through the docs unit tests (446 passed, 1 skipped) and failed only test_readme_table_matches_original_contract_index_snapshot on unchanged files; existing tracker bob-cli-hs owns that clean-base digest mismatch.

[2026-11-06T09:10:40Z · bob-cli-hg.6.1.3] Implemented Gmail save/refresh CLI and staged transaction API with writer and parent checks, locked replanning, atomic note/image writes, scoped Git recovery, post-commit journals, catalog/completion coverage, and docs. Verified cargo fmt --check, just lint, 16 gmail_shell tests, 3 image installer unit tests, and focused completion coverage. just check remains red only on clean-base clipboard duplicate tests (bob-cli-hp) and stale root-help snapshots (recorded in bob-cli-hg.6.1.1 note #1); just docs-check remains red only on the unchanged README contract-table digest test (bob-cli-hs). epic-symbols was clear.

## Dependencies

- **Depends on:** [bob-cli-hg.6.1.2](bob-cli-hg.6.1.2.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hg.6.1.4](bob-cli-hg.6.1.4.md) ✓ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-hg.6.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.6.1.3/README.md) | [bob-cli-hg.6.1.3](bob-cli-hg.6.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b70a8fb`](https://github.com/bobs-org/bob-cli/commit/b70a8fbffd809aed3aae33f4183de93d99ce3bf9) | feat(gmail): add transactional save and refresh | [bob-cli-hg.6.1.3](bob-cli-hg.6.1.3.md) | 2026-11-06 04:12:14 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hg.6.1.3][1] | Confirm the final phase scope, decisions, and recorded verification before closing | 3 |
| read-by | [agent:bob-cli-hg.6.1.land--1][2] | Recheck child scope, closure notes, and original follow-up disposition for epic closeout | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.6.1.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-hg.6.1.land.md

<!-- sase:referenced-by:end -->
