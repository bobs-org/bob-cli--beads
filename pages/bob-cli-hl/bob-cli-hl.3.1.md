# Bead: bob-cli-hl.3.1 — Complete capture merge-in execution for bob-cli-hl.3

[Bead Pages](../README.md) / [bob-cli-hl.3](bob-cli-hl.3.md) / bob-cli-hl.3.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-hl.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hl.3.md) · **Assignee:** `bob-cli-hl.3.1.land`
**Created:** 2026-11-05 19:49:41 EST · **Closed:** 2026-11-06 01:34:13 EST
**Plan:** [202611/capture\_merge\_in\_execution.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_merge_in_execution.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/capture_merge_in_execution.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_merge_in_execution.md

<!-- sase:links:end -->

## Description

Capture < creates its target and merges every source atomically, with accurate previews, offers, teaching errors, and verified CLI output.

## Notes

[2026-11-06T06:34:13Z · bob-cli-hl.3.1.land] LANDED bob-cli-hl.3.1 (capture `<` merge-in execution). Verified all five phases closed and read their commits: 4282e712 (adapter: plan_explicit_merge + capture-wide task births), fd26fb29 (origins: serde-skipped merge_line_origins -> task_blocks lines[].origin), fbb6da46 (feedback: merge_in_pending, fd-0 shell_ate_merge_in_arrow, merge_source_closed teaching copy, new-target header, G2/G4/G5), 3fe50bc7 (execute: capture/merge_in.rs preflight + one explicit merge after T is staged, transitional merge_in_unavailable removed), 6af313b4 (acceptance: MI matrix, real-plan guarded-write rollback, docs markers). Decisions honored: pruned-source Pull-In title count, no memory edits, no version/CHANGELOG/grammar/schema bumps.

LANDING INTEGRATION (this commit): merge_in_pending and hl.4's `<` picker each re-implemented the engine's source eligibility rules. They now call shared task_merge helpers (source_identity_refusal, open_subtask_count, open_subtasks_refusal, closed_source_refusal), which also replace the engine's two inline copies. Pending rows now carry execution's exact code and message in engine order, including the already-merged teaching copy. Gaps closed: the MI16 reconcile test now covers scheduled, dependency-Blocked, and a real `:id` target (no offer, source pruned, reconcile no-op); the new-target human header is pinned (merge_in_human_output_prints_new_target_header_once); and a test pins pending/execution parity (merge_in_pending_mergeability_matches_execution_refusals). Fixed a clippy last() warning from 6af313b4. Docs: task-merge.md MI9/MI15/MI16/MI17 test names (MI16 cited a nonexistent name; now mg17_...), capture.md merge_in_pending mergeable fields, compatibility.md stale "transitional merge_in_unavailable" sentence.

GATES: just fmt + just lint pass. just check runs every test; only 7 pre-existing non-merge failures: lib every_table_entry_matches_the_tree and public_leaves_are_entries_or_excluded (clipboard), and CLI catalog::protocol_1 (73 vs 72), help::root_help (missing gmail row), and 3 capture::successor_verdicts. Focused suites: merge_in CLI 32/32, task_merge lib 52/52, capture_complete lib 143/143; the full capture:: CLI run had only the 3 successor_verdicts failures. just docs-check: everything passes except test_readme_table_matches_original_contract_index_snapshot (docs/README.md last changed in 81e0d0c2).

FOLLOW-UP TRIAGE: +1 bob-cli-hp (clipboard; hl.3.1.3 #1, hl.3.1.4 #1, hl.3.1.5 #2); +1 bob-cli-de (catalog count; hl.3.1.3 #2); +1 bob-cli-hs (README hash; hl.3.1.5 #1). Root-help snapshot (hl.3.1.3 #4 said gkeep, but the missing row is gmail): DISCOVERED ISSUE corroboration on active epic bob-cli-hg (already its note #2). successor_verdicts (hl.3.1.5 #2): DISCOVERED ISSUE on active epic bob-cli-hn (efbe3470 tests vs 44c5c8c8 offer_close copy). Declined as already resolved: unused TODAY const (hl.3.1.1 #1, hl.3.1.2 #1), grammar 14-vs-15 docs drift (hl.3.1.2 #2), note_pull offer.close fixtures (hl.3.1.3 #3), lychee task-merge anchor (hl.3.1.4 #2). Not filed: the always-zero arrow_rel_start helper in hl.2's capture_language/draft.rs (cosmetic, no behavior impact). No epic symbols.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-hl.3.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hl.3.1.land/README.md) | [bob-cli-hl.3.1](bob-cli-hl.3.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`248a2bf`](https://github.com/bobs-org/bob-cli/commit/248a2bfa3b53e68d02e5f4976f76c75e3575add1) | refactor(capture): share merge source eligibility with merge-in pending and picker | [bob-cli-hl.3.1](bob-cli-hl.3.1.md) | 2026-11-06 01:35:29 EST |
| bob-cli--plans | [`bob-cli--plans@1c331fb`](https://github.com/bobs-org/bob-cli--plans/commit/1c331fb6ad840c4f10f2b7834b60b640ddbde1e6) | chore(plans): mark capture\_merge\_in\_execution done | [bob-cli-hl.3.1](bob-cli-hl.3.1.md) | 2026-11-06 01:35:53 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hl.3.1.1--2][1] | Need governing epic decisions before closing its assigned phase | 1 |
| read-by | [agent:bob-cli-hl.3.1.2][2] | Need parent epic decisions | 1 |
| read-by | [agent:bob-cli-hl.3.1.4][3] | Need parent epic plan and decisions | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hl.3.1.1.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hl.3.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hl.3.1.4/README.md

<!-- sase:referenced-by:end -->
