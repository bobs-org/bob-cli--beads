# Bead: bob-cli-on.8.1 — Requirements on the capture successor card

[Bead Pages](../README.md) / [bob-cli-on.8](bob-cli-on.8.md) / bob-cli-on.8.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-on.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.8.md) · **Assignee:** `bob-cli-on.8.1.land`
**Created:** 2026-11-22 07:22:29 EST · **Closed:** 2026-11-22 14:47:55 EST
**Plan:** [202611/requirement\_close\_engine.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/requirement_close_engine.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/requirement_close_engine.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/requirement_close_engine.md

<!-- sase:links:end -->

## Description

Complete bob-cli-on.8: managed capture Done closes audit each owner's pending requirements, apply explicit drop/carry/pull-in choices atomically, reject stale or overlapping choices, and report the final navigation and outcomes to clients.

## Notes

[2026-11-22T19:09:08Z · bob-cli-on.8.1.land] Land review (step 3 follow-up triage): the only PROPOSED FOLLOW-UP (bob-cli-on.8.1.4 note #2, req_verdicts overlap/fold ancestry skips hand-ticked intermediates) is CAUSED BY THIS EPIC, so no task bead was filed; it is remaining epic work in the landing tale. Reproduced at 96a23f50: ancestor -X plus descendant -k across a hand-ticked [x] row commits both writes (should refuse req_verdict_overlap); ancestor -k plus descendant -X refuses as req_close_stale instead of req_verdict_overlap. Other land-review findings, also epic-caused and folded into the same tale: (a) the capture req post-pass passes closing: None, so on a Pomodoro close (x!) a carry-pulled task skips the closing continuation that ordinary successors use (repro: -p 1 creates a separate CHORE entry while an ordinary -p pick lands in the created CAPTURE continuation); closing_after_successors is unused outside tests; (b) module-level cfg_attr(not(test), allow(dead_code)) remains on task_complete::{req_close,req_landing,req_placement,req_verdicts,req_writes}, contrary to the plan's no-permanent-suppression rule (10 unused items surface when removed); (c) tests/cli/capture/req_close.rs pull_in_on_req_is_carry_pulled has an always-true day-file assertion. Integration: post-start non-epic commits a21fd556 (albums index_group_by), b7945e75 (SO33 docs, conflict copies), c833be00 (release v0.6.0) need no integration with the requirement close engine.

[2026-11-22T19:47:55Z · bob-cli-on.8.1.land] Phases 8.1.1–8.1.6 reviewed closed. Landing tale plan:202611/req_close_landing_fixes.md implemented on HEAD 96a23f50 (host finalizer commits): overlap and fold now walk owner.nodes so ancestor/descendant choices across a hand-ticked [x] intermediate refuse req_verdict_overlap (RV44, overlap_across_hand_ticked_intermediate_refuses_both_orders); Pomodoro close x! carry+pull-in uses ClosingContext via ReqClosingPlacement, closing_after_successors, and line_maps forwarding (pomodoro_close_pull_in_uses_the_closing_continuation, multi-carry, later_item_still_places_a_pomodoro_close_carry); five permanent cfg_attr(not(test), allow(dead_code)) suppressions on req_* modules removed and unused items gated #[cfg(test)] with no new allow(dead_code) or --epic-symbol exemptions; pull_in_on_req_is_carry_pulled now asserts carried.block_id handles-empty-input and [[sase#^handles-empty-input]]. just check passed (fmt, clippy -D unused, workspace tests). just docs-gen produced no unexpected diff. just docs-check passed. Integration of a21fd556, b7945e75, c833be00 needed nothing. The only PROPOSED FOLLOW-UP (8.1.4 #2) was epic-caused and fixed here.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.8.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.8.1.land.md) | [bob-cli-on.8.1](bob-cli-on.8.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`c72c941`](https://github.com/bobs-org/bob-cli/commit/c72c941deb7329e65e1899ae475a55136fe80f79) | fix(capture): land requirement-close overlap, x! pull-in, and dead-code cleanup | [bob-cli-on.8.1](bob-cli-on.8.1.md) | 2026-11-22 14:51:26 EST |
| bob-cli--plans | [`bob-cli--plans@04adcf3`](https://github.com/bobs-org/bob-cli--plans/commit/04adcf3c2e5368e1cff71509080e9b98c8106d8a) | docs(plans): mark requirement\_close\_engine done after bob-cli-on.8.1 land | [bob-cli-on.8.1](bob-cli-on.8.1.md) | 2026-11-22 14:52:27 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-on.8.1.1][1] | Need parent epic DECISIONS and phase scope | 1 |
| read-by | [agent:bob-cli-on.8.1.3][2] | Need parent epic scope and decisions | 1 |
| read-by | [agent:bob-cli-on.8.1.4][3] | Need the epic decisions and phase list | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.8.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.8.1.3/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.8.1.4/README.md

<!-- sase:referenced-by:end -->
