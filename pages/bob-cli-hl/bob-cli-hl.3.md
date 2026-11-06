# Bead: bob-cli-hl.3 — One-transaction execution, output, and copy fixes

[Bead Pages](../README.md) / [bob-cli-hl](README.md) / bob-cli-hl.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.190](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.190.md) · **Assignee:** `bob-cli-hl.3` · **Size:** large
**Created:** 2026-11-05 18:05:40 EST · **Closed:** 2026-11-06 01:34:13 EST
**Plan:** [202611/capture\_merge\_in\_arrow.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_merge_in_arrow.md)

## Description

execute: stage the new task, then run one explicit merge into it through a helper lifted from the `>` path; report merges, offers, origins, and pending context; fix bob-cli-hi merge copy; add the shell guard.

## Notes

[2026-11-06T06:34:36Z · bob-cli-hl.3.1.land] PHASE VERIFICATION (bob-cli-hl.3.1.land): child epic bob-cli-hl.3.1 completed the whole execute phase of plan:202611/capture_merge_in_arrow.md: T < S1..Sn stages the new task, then runs one explicit merge into it through the shared plan_explicit_merge helper (commits 4282e712, fd26fb29, fbb6da46, 3fe50bc7, 6af313b4, plus the landing commit sharing engine source eligibility with merge_in_pending and the < picker). Execute-owned MI rows MI1-MI6, MI9-MI17 map to executable tests in docs/task-merge.md; merge_in CLI 32/32, task_merge lib 52/52. Also verified: shell guard (shell_ate_merge_in_arrow_refuses_argv_with_at_stdin_redirect, shell_ate_merge_in_allows_plain_files_pipes_and_stdin_capture); task_blocks origin and target.created (transfer origins tests, merge_in_creates_target_and_appends_sources_after_authored_notes); merge_in_pending (merge_in_pending_* tests). bob-cli-hi CLOSURE EVIDENCE for the outer land agent: G2 label merges print the merge block once with relations retained (tests/cli/capture/relations_merge.rs label_merge_human_output_prints_merge_block_once_with_relations); G4 singular copy title only / 1 note moved / N notes moved (task_merge lib matrix in src/native/task_merge/tests.rs; merge_in_human_output_prints_new_target_header_once asserts '1 note moved'); G5 Pull-In title counts only merged sources with links_pruned > 0 (tests/cli/capture/transfer.rs transfer_records_serialize_merge_offers_top_copy_and_move_fields: one qualifying source gives Link “T” in place of “S”). Gates: just fmt and just lint pass. just check has only 7 pre-existing non-merge failures: clipboard -> bob-cli-hp, catalog 73/72 -> bob-cli-de and bob-cli-hg, root help gmail row -> bob-cli-hg, 3 successor_verdicts -> bob-cli-hn. just docs-check fails only the README contract hash -> bob-cli-hs. No epic symbols. bob-cli-hi and bob-cli-hl remain open for their own land agents.

## Dependencies

- **Depends on:** [bob-cli-hl.2](bob-cli-hl.2.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hl.5](bob-cli-hl.5.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hl.6](bob-cli-hl.6.md) ✓ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-hl.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hl.3.md) | [bob-cli-hl.3](bob-cli-hl.3.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hl.3.1.4][1] | Need epic DECISIONS governing phase work | 1 |
| read-by | [agent:bob-cli-hl.3.1.land][2] | Need the parent phase scope and notes for later closure | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hl.3.1.4/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hl.3.1.land/README.md

<!-- sase:referenced-by:end -->
