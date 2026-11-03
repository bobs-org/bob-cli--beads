# Bead: bob-cli-gj.2.1 — Implement note-pull capture in bob-cli

[Bead Pages](../README.md) / [bob-cli-gj.2](bob-cli-gj.2.md) / bob-cli-gj.2.1

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-gj.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-gj.2.md) · **Assignee:** `bob-cli-gj.2.1.land`
**Created:** 2026-11-03 12:31:13 EST
**Plan:** [202611/note\_pull\_cli.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/note_pull_cli.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/note_pull_cli.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/note_pull_cli.md

<!-- sase:links:end -->

## Description

Complete bob-cli-gj.2 with atomic explicit note-pull selection, grammar 7, shared pull-in reporting, NP1–NP28 coverage, and real-bob fixtures for the Mac phase.

## Notes

[2026-11-03T20:17:27Z · 17p] DISCOVERED ISSUE: this epic's phases broke the bob-cli build (just install) twice on 2026-11-03. (1) c673d144 (bob-cli-gj.2.1.1) added the required CaptureItemResult.note_pull field but missed the sub-bullet literal that 3b1cf138 (agent 17i) had just added in plan_capture_item, which caused a missing-field compile error. Agent 17l fixed it in 9a606395 by putting note_pull: None first. (2) a95d5d8f (bob-cli-gj.2.1.2) added note_pull: None as the last field of the same literal on a base without 9a606395. The rebase applied cleanly because the hunks are about 80 lines apart, which left E0062 "field note_pull specified more than once". The fix commit drops the trailing copy and keeps the leading one, which matches every other literal. Both phases passed tests on their pre-rebase base, and nothing compiled the rebased tip. Land agent: run cargo check --all-targets --locked on the master tip after each phase lands. bob-cli-gh.8's PROPOSED FOLLOW-UP #1 is the same first breakage, already fixed by 9a606395.

[2026-11-03T20:58:35Z · 17p.f0] DISCOVERED ISSUE (third build break): 3d1822be (bob-cli-gj.2.1.3) broke just install again with E0063 "missing field note_pull" in plan_capture_item's sub-bullet CaptureItemResult literal (src/native/capture/plan.rs). The phase deleted the leading note_pull: None to fix the E0062 duplicate on its stale base, while e74f4f08 had just deleted the trailing copy on master. The two deletions are about 80 lines apart, so the landing rebase applied both cleanly and left none. The fix commit restores the leading copy, which makes plan.rs byte-identical to e74f4f08's version. All three of today's breaks share one mechanism: an agent edited this literal on a stale base, verified it only there, and the rebased tip was never compiled. Break 1 (c673d144, E0063) was a new required field vs. a concurrently added literal. Breaks 2 (a95d5d8f, E0062) and 3 (3d1822be, E0063) were each a concurrent fix of the previous break colliding with another fix, both adding and then both deleting. The COORDINATION NOTE on bob-cli-gj.2.1.3 arrived at 15:17:34, after the phase read its bead at 14:58:50, so bead notes do not reach a running phase. bob-cli-gj.2.1.4 runs on base 3d1822be (no note_pull) and will hit this E0063. If it re-adds the line anywhere but the leading position, the rebase leaves a duplicate (E0062, a fourth break). Land agent: before closing this epic, confirm cargo check --all-targets --locked passes on the master tip and that this literal has exactly one note_pull, in the leading position.

[2026-11-03T22:37:45Z · bob-cli-gj.2.1.land] LANDING AUDIT at 093dcead: read both epic notes and all 12 notes on phases .1-.4; inspected c673d144, a95d5d8f, 3d1822be, 093dcead and their current parser/planner/presentation/fixture source. The initializer repair notes are addressed in source: plan_capture_item sub-bullet CaptureItemResult has exactly one leading note_pull: None (de01143e); a fresh cargo check --all-targets --locked is still required before closing. Accepted open_lanes/refuse/no-memory decisions are preserved. No epic-symbol entries. Epic stays open: code review identifies fold-proof gating, selected repeated-pull ownership, blocked-project reason counts, and CLI hint contract gaps; phase .4 also records 82.60 ms p95 against the accepted <=70 ms budget. These require a bounded repair tale, not closure.

[2026-11-03T22:37:50Z · bob-cli-gj.2.1.land] FOLLOW-UP TRIAGE completed with /sase_new_task. Proposal from bob-cli-gj.2.1.2 note #1 (8 nonminimal-bool errors / result_large_err under -D warnings): declined as a new task. The canonical justfile lint/check deny list excludes both advisory classes and does not use -D warnings (confirmed by just --dry-run lint); .4 reports a later canonical check pass. No failure of the actual gate was supplied. Searched ci tasks then all task types, swept last-week tasks, inspected active epic scopes and bob-cli-fh; fh is a distinct needless_return report, so no speculative +1. Proposal from bob-cli-gj.2.1.4 note #3 (dependency-snapshot latency): retained as this epic work. The approved parent plan section 3.11 and child plan section 7 require the note-pull <=70 ms budget; 82.60 ms is not acceptance. Read bob-cli-gc: it tracks a pre-existing !-close baseline, not this newly added @route path, so no duplicate task or unsupported corroboration. Both proposal outcomes are final for the repair tale close note.

[2026-11-03T22:37:54Z · bob-cli-gj.2.1.land] INTEGRATION AUDIT: examined all non-epic commits c673d144^..093dcead plus earlier commits after epic creation. Clipboard direct-child capture 3b1cf138 caused the initializer collision now repaired; preserve its leading initializer. Ordered move adapter cf1e4644 changes transaction ordering and is not yet wired to project-note execution; b94eec2c retains the explicit staged guard. b8688d9e advances grammar to 8 with parser/help/docs alignment; do not restore 7. Target-run staging d1f34842 remains disabled in production, so preserve its option and recheck activation drift (parent bob-cli-gj notes reserve revision 9 for gm activation). Attachment origin writes 0b4cebdf are clip-only; lone pulls carry no clip. Period migration/reports/reviews, pomodoro --last, TODAY docs, and merge/split contract-only changes add no note-pull-specific integration path. Recheck newly landed code in the repair tale, and use the staged day/path helpers and shared transaction ordering. This is direct master workflow, no PR base branch.

[2026-11-03T23:30:28Z · bob-cli-gj.2.1.land] Repair tale progress: fixed fold-proof gating (hidden/scheduled/live with closed prerequisites now fold correctly via narrowed vault proof), proven project-block counts (1 open of 2 reports 1 task, staged closes visible), selected repeated-pull ownership (All/numeric/key/ID-less/duplicates prune via stable keys and post-mint block IDs; explicit-link empties still refuse), cross-group earliest-wins dedup across hand_off/relation/note-pull, and pull-only hint first/last numbers (-p 1,3). Fixtures regenerated (np1 human hint -p 1,3), new unit regressions (fold_gating, blocked_project_counts, repeated_selected_ownership, selected_handoff) plus CLI subset/two-note/mixed assertions pass. Gates: cargo check --all-targets --locked passes; just docs-check passes; focused note_pull (38) + CLI note_pull (7) + capture_language (556) pass. just check still fails on pre-existing catalog document_shape (69 vs 67) and protocol_1, reproduced on clean base, unrelated to this repair. Latency (release, isolated 6906-note vault): sase p95 87.67ms vs 70ms target (miss), mac_inbox 63.98ms meets. Narrowed proof (source + needed-ID substring retention) did not reach target on SSD temp; /tmp manual shows 63ms (meets) vs SSD 87ms, pointing to file-open/metadata cost for 6906 files per process. No stale cache, safety proof, or threshold weakening introduced. Blocker recorded; epic stays open per step 4.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-gj.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-gj.2.1.land.md) | [bob-cli-gj.2.1](bob-cli-gj.2.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4db3200`](https://github.com/bobs-org/bob-cli/commit/4db3200cd6367c43a252322b66e3c6652e8a7295) | fix(capture)!: finish note-pull contract and landing | [bob-cli-gj.2.1](bob-cli-gj.2.1.md) | 2026-11-03 18:32:59 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-gh.8][1] | Determine whether the existing note-pull phase tracks the clean-base compiler failure | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gh.8/README.md

<!-- sase:referenced-by:end -->
