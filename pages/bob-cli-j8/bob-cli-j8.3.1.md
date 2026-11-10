# Bead: bob-cli-j8.3.1 — Notebook routes write notes

[Bead Pages](../README.md) / [bob-cli-j8.3](bob-cli-j8.3.md) / bob-cli-j8.3.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-j8.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-j8.3.md) · **Assignee:** `bob-cli-j8.3.1.land`
**Created:** 2026-11-09 13:50:25 EST · **Closed:** 2026-11-09 22:35:43 EST
**Plan:** [202611/notebook\_capture\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/notebook_capture_notes.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/notebook_capture_notes.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/notebook_capture_notes.md

<!-- sase:links:end -->

## Description

Complete bob-cli-j8.3 with shared notebook capture parsing, guarded note writes, accurate previews, opt-in targets, and verified contracts.

## Notes

[2026-11-10T01:43:02Z · bob-cli-j8.3.1.land] LAND AUDIT at 12692ebb (origin/master fetched and equal): read all four children and every note, child plan and binding parent plan/DECISIONS, and actual source/commits d9066754, 3f8c49d4, 8d098e55, 12692ebb. All four children are closed; no PROPOSED FOLLOW-UP entries exist. The implemented parser, list/global/forced routes, guarded writer, opt-in scanner and related-task filtering are present, and transitional execution refusal is gone, but their completion claims do not cover the remaining defects below. The accepted shared span contract was not honored: notebook_* span kinds replace the promised existing labels plus notebook modifier. Section resolution is writer-private, so near-miss diagnostics are absent from parse. Child-note nesting, task-shaped authored bullets, live-anchor identity and complete read guards also need repair. Exact-source Rust probes confirmed split_lines_keep/join_lines transforms CRLF into CRCRLF and region_bounds/last_note_block_end_in_region selects insertion inside a fenced example. Source review additionally found sub-note detail/clipboard indentation at the new note's level; duplicate parent IDs are counted only among eligible bullets and repeated new sub-note IDs are not checked; plain notes mentioning #task are rejected as parents; owner-chain bytes are discarded instead of becoming read guards; a leading %c before a leading notebook route can discard the note body. Existing CLI tests cover 11 happy/refusal cases, not the required CRLF/retype/clipboard rollback matrix. No full just check was run in this planning turn and the installed executable was not used as evidence for HEAD. Planning a bounded medium tale for these epic-caused defects plus final landing, not separate tasks.
Integration: reviewed all 12 intervening non-epic commits d7906813, a846a23b, b97d8d4c, 0ed552a5, b5196709, 0996111c, 076fdc48, 2327590f, 8728fe28, 03dfe6de, 6d063ff5, eba2bd59. Archive pairing/readers/stats changes do not require notebook task homes; retain the opt-in scanner invariant and current guarded transaction. The later task-merge fix's live-anchor/code distinction is directly relevant to the new notebook writer's duplicate parsing and must be reflected in repair tests. Dot separator typing remains lexical; retain those existing regressions and leave the accepted @ collapse/new picker UI to sibling j8.5. No current source integration edits were made. No --epic-symbol entries for bob-cli-j8.3.1. Research artifact remains missing after audited retry; the approved plans are binding.
FOLLOW-UP TRIAGE: no child proposals to accept or decline. One independent pre-existing checker defect discovered by this lander (rules.rs::extract_block_ids counts inline-code/wiki-reference carets) was processed through /sase_new_task, with same-type and all-type duplicate searches and one-week sweeps; no duplicate. Recorded DISCOVERED ISSUE with executable probe evidence on active causal parent bob-cli-j8 (introduced by j8.1/0a74731b); no new task under the active-epic rule. The repair tale must repeat this outcome in the epic close note. bob-cli-j8.3 remains open until this child epic is truly fixed; leave containing bob-cli-j8 to its own land agent.

[2026-11-10T01:47:29Z · bob-cli-j8.3.1.land] REMAINING-WORK PLAN: sase_plan_notebook_capture_landing_repairs.md is a medium tale for one coder to repair the existing notebook writer/parser/policy, run focused tests plus just check/docs checks, and perform delegated closeout of this epic then phase bob-cli-j8.3 in the same turn as the final code. It does not depend on its own future commit/push/CI. Further source review confirms global notebook fallback currently precedes explicit standalone %n/session parsing (draft.rs::parse_capture_item_members and notebook.rs::classify_item); the tale includes preserving explicit operation modes under @nb. All four original child notes and the epic/parent decisions were reviewed; creation/assist/Mac/memory scope remains with the wider epic. Triage is complete: no child PROPOSED FOLLOW-UP entries, all capture-caused defects remain epic work, and the sole pre-existing checker issue is recorded on active parent bob-cli-j8 with no duplicate/new task. No epic or phase has been closed and the epic plan stays wip pending repair. The tale requires rechecking symbols, source and post-audit drift, normal descendant closure, normal epic closure, symvision if available, setting 202611/notebook_capture_notes.md done through the opened plans repo, and normal closure of bob-cli-j8.3 only. The current justfile has no symvision recipe.

[2026-11-10T03:35:43Z · bob-cli-j8.3.1.land] Verified all four closed descendants, the approved plans, decisions, repaired findings, and no child proposals. Repairs preserve LF/CRLF and final-newline bytes; resolve real headings/fences and sections consistently; scan anchors globally and validate new IDs; nest authored/clipboard details correctly; refuse notebook checkboxes; preserve explicit operations and the leading %c body; guard route metadata bytes; and restore the established span labels with notebook=true under grammar 24. Focused verification passed: 87 notebook unit tests, metadata drift guard, 18 notebook CLI tests, 1,837 capture CLI tests, and 5 JSON shape tests. just docs-gen passed. just check exits 101 only for native::task_merge::tests::mg18_merge_source_with_descendant_anchor_archives_through_bound_pair (6,245 library tests passed, 1 failed, 3 ignored); isolated reproduction is recorded on active causal epic bob-cli-j5 with artifact file:explicit:82c6a707ddd506f8b0f9d403. just docs-check remains blocked by the bob-mac-capture index.md mount collision. No just symvision recipe; epic-symbols has no entries for this epic or parent phase. Preserve the prior extract_block_ids checker issue on causal parent bob-cli-j8 with no new task, per existing triage. No new task bead was created. The linked epic plan status is done.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-j8.3.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-j8.3.1.land.md) | [bob-cli-j8.3.1](bob-cli-j8.3.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`843642f`](https://github.com/bobs-org/bob-cli/commit/843642f9fc34e0edf60b126751bb221d2fe6283c) | feat(capture)!: repair notebook capture landing | [bob-cli-j8.3.1](bob-cli-j8.3.1.md) | 2026-11-09 22:37:58 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-j8.3.1.2][1] | Need parent epic DECISIONS and phase list | 1 |
| read-by | [agent:bob-cli-j8.3.1.3][2] | Need parent epic scope | 1 |
| read-by | [agent:bob-cli-j8.3.1.4][3] | Need parent epic scope for closure evidence | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-j8.3.1.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-j8.3.1.3/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-j8.3.1.4/README.md

<!-- sase:referenced-by:end -->
