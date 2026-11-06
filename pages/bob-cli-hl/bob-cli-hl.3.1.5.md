# Bead: bob-cli-hl.3.1.5 — Prove equivalence, rollback, and final contract coverage

[Bead Pages](../README.md) / [bob-cli-hl.3.1](bob-cli-hl.3.1.md) / bob-cli-hl.3.1.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-hl.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hl.3.md) · **Assignee:** `bob-cli-hl.3.1.5` · **Size:** medium
**Created:** 2026-11-05 19:49:42 EST · **Closed:** 2026-11-06 00:59:38 EST
**Plan:** [202611/capture\_merge\_in\_execution.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_merge_in_execution.md)

## Description

acceptance: complete the MI execution matrix, byte-equivalence and reconcile tests, actual guarded-write rollback coverage, and shipped documentation markers; prepare verified closure evidence for the child epic land agent.

## Notes

[2026-11-06T05:32:33Z · bob-cli-hl.3.1.5] PROPOSED FOLLOW-UP: Refresh the docs README contract-table snapshot hash — `just docs-check` reaches the documentation unit tests but test_readme_table_matches_original_contract_index_snapshot fails (expected fedc20a035e78ecfd201ce2462d2eccb1683046f66c749477949287aade4fe72, got 96a429d5f5b7eb02484e4806dac0ca688e41858e3187dfbdb26ad994a6107e4a); git diff --quiet HEAD -- docs/README.md tools/docs/tests/test_contracts.py exited 0, so the failing assertion reads unchanged clean-base files. No matching bead exists.

[2026-11-06T05:59:16Z · bob-cli-hl.3.1.5--2] PROPOSED FOLLOW-UP: Repair the clean-base failures reproduced at 3fe50bc75ef4b6c7ef35d878b4f881b7df1d2128 — `cargo test -p bob-obsidian --lib` fails native::catalog::tests::public_leaves_are_entries_or_excluded (clipboard in both lists) and native::completion::kinds::tests::every_table_entry_matches_the_tree (duplicate clipboard:count); `cargo test -p bob-obsidian --test cli` fails capture::successor_verdicts::{done_verdict_resolves_root_only_with_scope_note,ineligible_verdicts_refuse_with_why,new_task_verdicts_refuse_write_free}, catalog::protocol_1_parses_with_schema_version_one, and help::root_help_matches_sectioned_short_and_long_snapshots. These are the same seven failures from `just check` on the phase tree; clean-base command was `set +e; cargo test -p bob-obsidian --lib; lib_status=$?; cargo test -p bob-obsidian --test cli; cli_status=$?; ...`.

[2026-11-06T05:59:38Z · bob-cli-hl.3.1.5--2] Verified merge-in acceptance coverage for source ordering, byte-equivalence, atomic refusals, dependencies, offer suppression, task-list writes, reconciliation, JSON origins, and shared-dependent human summaries. The injected guarded-write rollback test passed and verified restoration of source, dependent, daily ledger, new target, and temporary files. Focused suites passed: merge-in CLI (30), transfer CLI (30), capture unit tests (153), and task-merge unit tests (52); just fmt passed. just docs-check has the clean-base README contract snapshot failure already recorded as a proposed follow-up. Full just check failed in two library and five CLI tests; all seven reproduce on clean base 3fe50bc75ef4b6c7ef35d878b4f881b7df1d2128 and are recorded as a proposed follow-up. Epic-symbol check is clear.

## Dependencies

- **Depends on:** [bob-cli-hl.3.1.3](bob-cli-hl.3.1.3.md) ✓ · ⧖ 2026-11-05
- **Depends on:** [bob-cli-hl.3.1.4](bob-cli-hl.3.1.4.md) ✓ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-hl.3.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hl.3.1.5.md) | [bob-cli-hl.3.1.5](bob-cli-hl.3.1.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`6af313b`](https://github.com/bobs-org/bob-cli/commit/6af313b4d36460174ff6b951e208653ea0160afc) | test(capture): complete merge-in acceptance coverage | [bob-cli-hl.3.1.5](bob-cli-hl.3.1.5.md) | 2026-11-06 01:00:42 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hg.12.1.1][1] | Check whether the existing follow-up covers the identical README contract-table snapshot failure | 1 |
| read-by | [agent:bob-cli-hl.3.1.4][2] | Check acceptance phase to avoid overlap | 1 |
| read-by | [agent:bob-cli-hl.3.1.5--2][3] | Need the phase scope, decisions, design file, and prior notes before finishing acceptance verification | 1 |
| read-by | [agent:bob-cli-hl.3.1.land][4] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hg.12.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hl.3.1.4/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hl.3.1.5.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hl.3.1.land/README.md

<!-- sase:referenced-by:end -->
