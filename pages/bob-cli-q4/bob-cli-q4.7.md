# Bead: bob-cli-q4.7 — Task commands and sync writers settle their notes

[Bead Pages](../README.md) / [bob-cli-q4](README.md) / bob-cli-q4.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1fw](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1fw.md) · **Assignee:** `bob-cli-q4.7` · **Size:** medium
**Created:** 2026-11-25 08:51:36 EST · **Closed:** 2026-11-25 12:06:27 EST
**Plan:** [202611/better\_o\_gesture\_settle.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/better_o_gesture_settle.md)

## Description

command-settle: compose the settle helper into `bob task move`, `split`, `merge`, and `restore`, `bob gmail sync`, `bob ref create`, `bob gkeep pull`, and any other status- or residence-changing bob-cli writer the audit finds, with fixture proof that a later reconcile plans nothing note-local.

## Notes

[2026-11-25T17:05:52Z · bob-cli-q4.7] AUDIT LIST (command-settle writer audit, src/native): wired settle-before-staging into: task move (source+dest+link-repaired; restore shares the pipeline) in task_move/command.rs; task split in task_split/command.rs; task merge in task_merge/command.rs; gmail sync in gmail/sync/file.rs build_attempt (settles staged .md pre-hash, remaps reported watch/reopen rows via line_map); ref create + ref sync routed task writes in highlights_ref/sync.rs execute_routed_intents (intake funnels through plan_single_pdf_sync, so one site covers both); reading-task insert in ref_tasks/insert.rs; reading-task checkbox edit in ref_tasks/edit.rs (added bob_dir param, updated 13 test call sites + reading_execute.rs caller); gkeep pull in gkeep/pull.rs (all 3 insert_task_line sites settled pre-transaction). NOT switched per plan byte-identity gate: reroll (randomize_plan.rs) and archive/collect_done (collect_done/plan.rs) already group via transform directly; settle would add the local future-schedule [?] rule and change bytes, so reconcile still heals [?] rows there. Capture write path untouched (owned by q4.6 capture-settle; settle is idempotent so both compose safely). Task tidy out of scope per plan.

[2026-11-25T17:06:04Z · bob-cli-q4.7] PROPOSED FOLLOW-UP: lib test native::meetings::profile::tests::wispr_summary_renders_one_or_two_pages_with_stable_words fails on the clean base tree too (verified via git stash: fails with changes stashed, unrelated to command-settle which touches no meetings code). Needs a land-agent triage, not this phase.

[2026-11-25T17:06:09Z · bob-cli-q4.7] PROPOSED FOLLOW-UP: just docs-check fails on docs/reference/plugins/bob-navigation-hotkeys.md word budget (6068 words, cap 6000); file untouched by this phase and just docs-gen produced no diff, so pre-existing. Needs an owner to trim or re-budget.

[2026-11-25T17:06:27Z · bob-cli-q4.7] command-settle done and verified. Wired settle-before-staging into task move (+restore, shared pipeline), split, merge, gmail sync (with reported-row line_map remap), ref create/sync routed writes, reading-task insert+checkbox-edit, and gkeep pull (3 sites). Fixture proof: 7 new command_settle tests (move, restore, split, merge, gmail, gkeep, ref) assert settled postimages are settle fixed points, which q4.3 pins byte-identical to reconcile compose; live check: settled move then reconcile --dry-run plans nothing (marked_blocked/grouped/applied all empty), vs base binary leaving unsettled drift. Suites green: task_settle/move/split/merge/ref_tasks/gmail::sync/gkeep/highlights_ref/status_hooks lib tests, cli task_move/task_merge, gkeep_pull, gmail_shell, cli-gmail integration, cargo fmt, clippy gate, docs-gen (no diff). Pre-existing failures recorded as bead notes (wispr lib test fails on clean base; docs-check nav-hotkeys budget). No --epic-symbol entries. Full just check exceeds one-command time so verified in these pieces.

## Dependencies

- **Blocks:** [bob-cli-q4.13](bob-cli-q4.13.md) ◐ · ⧖ 2026-11-25
- **Depends on:** [bob-cli-q4.3](bob-cli-q4.3.md) ✓ · ⧖ 2026-11-25
- **Depends on:** [bob-cli-q4.5](bob-cli-q4.5.md) ✓ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q4.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.7/README.md) | [bob-cli-q4.7](bob-cli-q4.7.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q4.7][1] | Need full bead incl notes | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.7/README.md

<!-- sase:referenced-by:end -->
