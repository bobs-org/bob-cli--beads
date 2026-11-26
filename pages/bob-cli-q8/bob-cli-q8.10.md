# Bead: bob-cli-q8.10 — Finish one-tie-per-pair — counted absorption, atomic reversal, chord prompts, and the tie copy

[Bead Pages](../README.md) / [bob-cli-q8](README.md) / bob-cli-q8.10

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-q8.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-q8.land.md) · **Assignee:** `bob-cli-q8.10.land`
**Created:** 2026-11-26 02:09:19 EST · **Closed:** 2026-11-26 07:31:09 EST
**Plan:** [202611/finish\_plain\_link\_ties.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_plain_link_ties.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/finish_plain_link_ties.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_plain_link_ties.md

<!-- sase:links:end -->

## Description

Close the gaps the bob-cli-q8 landing found. Every nav dependency writer, counted sessions included, absorbs plain links. Depends-on and Blocks batches absorb on ↵ instead of refusing. Chords prompt for missing block IDs. A same-note reversal is one Ctrl+Z. The stage strips, hints, notices, and footers show the copy the approved plan specified. The shared PT and LR vectors cover what the docs claim.

## Notes

[2026-11-26T10:49:22Z · bob-cli-q8.10.land] LAND FOLLOW-UP TRIAGE: Read every note on bob-cli-q8.10.1, .2, and .3; there are no PROPOSED FOLLOW-UP entries and no distinct non-epic proposals to file or decline. LR35 excluding dry_run plus apply-only applied_files/recovery_directory is a justified documented clarification, not unaddressed work. Newly reproduced chord dispatch, block-ID prompt, and reversal composition defects remain this epic work and will be planned as a single medium tale, not filed as unrelated tasks.

[2026-11-26T10:52:48Z · bob-cli-q8.10.land] LAND VERIFICATION: Read all three child scopes/notes, both approved plans, governing decisions and q8 reviewer choices. Verified Rust commits 6e722fc6/1c23bce7/8cb474ba and plugin commits 6fb169bb/e82bd932/b4ab2cbb/561a9ea7/2cad24b7/b9b3cec9 against actual source. Shared tie fixtures match exactly; 62 focused plugin tests and build:check pass. No epic-symbol entries. Reviewed non-epic drift through CLI 292d60c0 and plugins 4ae966f4 (snooze, review, settle, caret/drawers, Bank/home ownership); no new tie representation/writer conflict found. Remaining epic blockers reproduced: cycle row strip offers Ctrl+B reversal but tieCommitChord immediately refuses disabled row; footer omits that same-direction reversing chord. ID-less marked row opens prompt before batch refusal. Both endpoints lacking IDs: confirmTieChangeBlockId writes owner ID, clears pending state, then fails with no tie because other still has no ID. Same-note reversal stamps the old first-parent line after second-plan insertions (a Depends-On drawer instead of Other) and loses secondPlan.summary.pomodoroTargets, skipping newly-blocked-owner cleanup. Current tests pass because relevant prompt/batch checks assert source text and writer case checks only edge/undo. A medium tale will fix these bounded paths, complete behavioral acceptance coverage/copy segments, then close q8.10 and recheck/close q8 in the coding turn. Both epics stay open pending repair; no force close.

[2026-11-26T11:02:44Z · bob-cli-q8.10.land] LAND TRIAGE ADDENDUM: Primary just check ToolRun 231f6b89bd79a9cbc17778a0ba1b3d92 on unchanged 292d60c0 passes fmt and gated Clippy and reproduces the established lib/CLI baseline (42+55 failures). /sase_new_task searches across statuses, recent-task sweeps, and active-epic/child reads confirm 80 drawer cases belong to bob-cli-ph and 17 settlement cases to bob-cli-q4; added corroborating DISCOVERED ISSUE notes to both, no duplicate task. WISPr passes, so no q9 corroboration. Relevant suites pass: task_relations 41/41, reconcile relations 49/49, capture relations 33/33. None of these unrelated failures expands the remaining tie tale. Child PROPOSED FOLLOW-UP inventory remains empty.

[2026-11-26T11:03:01Z · bob-cli-q8.10.land] FINAL CHECK RESULT: ToolRun 231f6b89bd79a9cbc17778a0ba1b3d92 completed exit 101 after all targets; only lib and CLI failed with the 97 already-triaged baseline cases. Other test binaries and doctests completed without a failing target. Formatting/gated Clippy passed. No check-full run. No product source or deployment was changed during this landing audit. The validated medium tale finish_tie_dispatch carries the remaining epic work and concrete q8.10/q8 closeout.

[2026-11-26T12:18:46Z · bob-cli-q8.10.land] FOLLOW-UP TRIAGE: No duplicate task or causally related active epic owns the separate bob-plugins npm run docs:check failure. The broad task search, recent-task sweep, and active epic list found only distinct nearby issues: bob-cli-it is the stale ignored mount collision, bob-cli-ot is an Intention Card runtime YAML failure, and bob-cli-oq was a broken docs anchor already fixed. The plugin docs gate deterministically rejects duplicate metadata keys in sase/memory/decisions/capture-bullets-mirror-the-task-block.md at the generated-drift stage after refreshing its bob-cli source to 9e94d1b1; bob-docs lint passes. Primary just docs-check passes. Filed bob-cli-qf (CI, ready) for the separate memory-frontmatter validation failure. It is outside q8 tie scope and does not block this epic.

[2026-11-26T12:31:09Z · bob-cli-q8.10.land] LAND VERIFICATION (q8.10): Implemented the dispatch, prompt, reversal-composition, counted absorption, and consequence-copy gaps. Read all three closed phase beads and notes; none has a remaining PROPOSED FOLLOW-UP. Reviewer choices remain ctrl_shift_l=yes, memory_decision_record=no, memory_glossary_relation=yes; the authorized glossary sentence already exists, and no memory files or Cargo version/changelog were changed. Verification: the five focused tie suites pass 69/69; npm test ToolRun 0959a52ca20fc30492fd6974fb9df9bb succeeded (243139 ms); npm run build passed. Bob-plugins npm run docs:check passes lint but its refreshed CLI checkout at 9e94d1b1 fails generated-drift YAML parsing on duplicate metadata in capture-bullets-mirror-the-task-block.md; task bob-cli-qf is ready, and the full new-task duplicate/weekly/active-epic triage found no duplicate or causal epic. Primary just docs-check ToolRun 9bd1e19df40877affac7ec040a10a139 passed all gates. Primary just check ToolRun 74f5bfe0905709a5e4d67f1fbf20b74a exited 101: fmt and gated Clippy passed; only lib and CLI failed (42/55), and the failed-test-name sets match prior ToolRun 231f6b89bd79a9cbc17778a0ba1b3d92 exactly. The 97 failures remain the already-routed drawer-cutover and settlement baseline; no tie target failed. bob plugins sync exited 0 without force, deployed bob-navigation-hotkeys and the already-built bob-ledger-tools bundle with backups at 20261126-071654; dry-run then reported 0 copies and 34 unchanged. No symvision recipe exists and epic-symbols is empty. Mac audit: q8.9 exact-SHA run 45749289760 on 797313af completed red on the previously tracked drawer failures; current linked Mac master 5949d253 CI run 45812847406 is green after those drawer fixes. No new tie writer or conflicting representation appeared in post-start CLI/plugin/Mac changes.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-q8.10.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-q8.10.land.md) | [bob-cli-q8.10](bob-cli-q8.10.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`bab65e6`](https://github.com/bobs-org/bob-cli/commit/bab65e60b7aff27d0d783eb95fc407c8e1609c16) | docs(tasks): document tie reversal effects | [bob-cli-q8.10](bob-cli-q8.10.md) | 2026-11-26 07:36:25 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q8.10.1][1] | need epic scope | 1 |
| read-by | [agent:bob-cli-q8.10.2][2] | Need parent epic scope for phase q8.10.2 | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-q8.10.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-q8.10.2/README.md

<!-- sase:referenced-by:end -->
