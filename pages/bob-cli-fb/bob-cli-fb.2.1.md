# Bead: bob-cli-fb.2.1 — Finish Rust leaf-project keep-moving offers

[Bead Pages](../README.md) / [bob-cli-fb.2](bob-cli-fb.2.md) / bob-cli-fb.2.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-fb.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-fb.2.md) · **Assignee:** `bob-cli-fb.2.1.land`
**Created:** 2026-11-01 13:00:27 EST · **Closed:** 2026-11-01 21:08:29 EST
**Plan:** [202611/leaf\_keep\_moving\_rust.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/leaf_keep_moving_rust.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/leaf_keep_moving_rust.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/leaf_keep_moving_rust.md

<!-- sase:links:end -->

## Description

Complete bob-cli-fb.2 with tested leaf detection, successor offers, capture selection and reporting, correct batch behavior, and verified performance.

## Notes

[2026-11-02T00:01:13Z · bob-cli-fb.2.1.land] LAND AUDIT / FOLLOW-UP TRIAGE before remaining-work tale: Read this epic (no prior notes), all notes on phases .1/.2/.3, the approved child plan and parent phase/epic decisions; reviewed commits f6d3084b, ab32d58a, 8347a46d and actual engine, capture callers, selection/net/rendering source and tests. All three phases are closed; offer_lanes=open is implemented Pending/Next/Ready, JSON remains schema 1, and these commits make no prohibited memory/version edits. No epic-symbol entries; this checkout currently has no symvision recipe. BLOCKERS: (1) snapshot_complete is only consulted by keep-moving classification. Both capture callers invoke the legacy planner even when the snapshot is unavailable, clear unblocked/still_blocked/project_folds afterward, then stage changed_files/new_day_text. A touched-note dependent on completed t plus external q can therefore recover or link from an incomplete graph while reporting no legacy rows. Existing KM31 fixture does not cover this same-note dependent. (2) keep-moving human rows use style_task_status_marker and tests pin raw [/] / [*] / [ ] despite the plan requiring lane names. (3) triggering keep-moving newly pays SuccessorTypeRouting::load/Catalog::load root-note scans; the phase reports about 45-55 ms additional cost and the absolute target miss. FOLLOW-UP OUTCOMES via sase_new_task: .2 note #1 lint proposal declined as already fixed by f490d88f (filter then map in actual capture_pomodoros_agenda.rs; reported filename was singular); no duplicate task. .3 note #1 split by cause: newly added routing/catalog cost remains this epic work; the pre-existing 70 ms close-path miss is already owned by active bob-cli-5w (landing notes #1/#2, .3/.4 proposals, and bob-cli-65 timing evidence), so appended attributed current evidence there, no new task and no reopening fixed 5v/6k/65. .3 note #2 CLI mock discrepancy retained as this epic documentation work: preserve existing destination capsules and make examples match the required named lanes. Searches covered all task statuses, recent-week tasks, and active epics. No proposal was dropped silently. INTEGRATION REVIEW: inspected non-epic commits since f6d3084b, especially Today roots b71a6c15 (exports root_label only; leaf resolver unchanged), MEET starts eda4dfc3, event warnings 273e09a7 (closes intentionally quiet), Work Log stamps 50df0e41, drawer grammar bbd26d97 and multi-note 5ac2fbc2 (shared planner/tracker ordering preserved), and merged routing primitives 675330dd (its active fe.2 still owns landing changes). 39804896 already repaired keep-moving lint/golden integration. Add focused combinations in the repair tale and recheck later drift. No fresh full check or timings were run by this audit; phase-reported passes/timings are not claimed as new results. Keep this epic and parent phase bob-cli-fb.2 open until the tale fixes, verifies, and closes them normally.

[2026-11-02T02:08:29Z · bob-cli-fb.2.1.land--1] Source: repairs on d712168f (audited 5ac2fbc2 + merged 3e21e990 R6 close-names + d712168f fe.2 merge; auto-merge clean on 4 overlapping files; fixed keep_moving_tests continuation_name rename). Dirty: docs/task-dependencies.md, src/native/capture/output.rs, pomodoro_close.rs, task_complete.rs, pomodoro_themes/mod.rs/scan.rs, task_complete/successors.rs, task_complete/tests/keep_moving_tests.rs, tests/cli/capture/keep_moving.rs (719+/161-). Decisions: offer_lanes=open (Pending,Next,Ready lane order, never raw symbols); JSON schema 1 additive with separate keep_moving arrays; no memory/version/flag/CHANGELOG edits; §12.15 lane names + retained (next up) capsule; §12.5 KM31 exception clarified. Integration: b71a6c15 (Today roots, leaf resolver unchanged), eda4dfc3/273e09a7 (MEET stays quiet), 50df0e41 (Work Log still offered), bbd26d97+5ac2fbc2 (multi-note ordering preserved), 675330dd (fe.2 planners, landing owned by fe.2), f490d88f (agenda lint fixed), 39804896 (keep-moving goldens fixed) all hold; new 3e21e990/d712168f integrated (ClosingContext continuation_name, merged landing). 5 typeless failures from 675330dd reproduced on 5ac2fbc2 clean base (missing [type::]), recorded on fe.5 note1 as owned by fe.2, now fixed by d712168f and verified 5/5 pass on merged tree. Tests: 36 keep-moving CLI pass, 159 task_complete lib pass incl routing_is_lazy_and_narrow (ROUTING_LOAD_COUNT 2 for 2 triggering, FULL_ROOT_SCAN_COUNT 0) and unavailable_snapshot_suppresses_all_legacy_writes, 5/5 named-link pass, docs-check 448 pass. Full just check on 5ac2fbc2+repairs: 2704 pass/5 pre-existing fail (proven identical on clean base); on d712168f+repairs just check stops at 6 pre-existing needless_return in task_theme.rs:706,709,735,748,758,760 (proven identical on clean d712168f via stash, routed as bob-cli-fh, not epic-added). JSON example: !perf_badges:t dry-run on 6546-md full copy gives keep_moving 3, trigger last_planned, group keep_moving, project perf_badges.md. Timing (release d712168f+repairs, apollo 16-core load ~16-20, 6546-md 2.1G temp copy, isolated config/clock, 50 reps dry-run json): triggering p50 198.7 min152.2 p90 245.1 max469.1 mean207.8; silent nontriggering p50 156.2 min113.0 p90 175.1 max246.6 mean156.7; hello p50 6.5ms. 70ms target missed; ~42ms delta is epic-added duplicate removed by lazy narrow routing (no full scans), remaining ~156ms floor is pre-feature and reported to bob-cli-5w (note 11/02). Proposals: .2 note1 declined as fixed by f490d88f; .3 note1 catalog cost repaired here + floor to 5w (no new task, no reopen); .3 note2 CLI mock repaired to lane names + retained capsule. Plan 202611/leaf_keep_moving_rust.md set done. Symvision unavailable (no just recipe).

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-fb.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-fb.2.1.land.md) | [bob-cli-fb.2.1](bob-cli-fb.2.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli--plans | [`bob-cli--plans@f703061`](https://github.com/bobs-org/bob-cli--plans/commit/f703061c6b4be2630f24a7b29afac68aa1eab2c4) | docs(plans): mark leaf\_keep\_moving\_rust done for fb.2.1 closeout | [bob-cli-fb.2.1](bob-cli-fb.2.1.md) | 2026-11-01 21:11:37 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-fb.2.1.2][1] | Need parent epic plan and DECISIONS | 1 |
| read-by | [agent:bob-cli-fb.2.1.land--1][2] | Need parent link before close | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fb.2.1.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-fb.2.1.land.md

<!-- sase:referenced-by:end -->
