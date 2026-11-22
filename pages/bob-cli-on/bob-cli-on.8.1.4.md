# Bead: bob-cli-on.8.1.4 — Carried-task pull-in and final jump resolution

[Bead Pages](../README.md) / [bob-cli-on.8.1](bob-cli-on.8.1.md) / bob-cli-on.8.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-on.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.8.md) · **Assignee:** `bob-cli-on.8.1.4` · **Size:** medium
**Created:** 2026-11-22 07:22:30 EST · **Closed:** 2026-11-22 11:08:26 EST
**Plan:** [202611/requirement\_close\_engine.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/requirement_close_engine.md)

## Description

placement: plan carried-task links at the existing successor destination, raise only pulled tasks to Next without stamping freshness, and resolve pinned requirement landings through carry and routing move maps.

## Notes

[2026-11-22T16:08:13Z · bob-cli-on.8.1.4] Handoff for bob-cli-on.8.1.5 (capture wiring). Engine: task_complete/req_placement.rs (pulled_tasks, closing_after_successors, plan_req_links; codes req_pull_in_no_destination, req_close_stale, req_jump_lost, req_jump_ambiguous) and task_complete/req_landing.rs (resolve_req_landing -> carried_task | moved_with_ancestor | requirement, effective outcome, final path/line). Adapter: capture/req_placement.rs plan_req_link_pass (records every carried task via record_created_task, links pulled carries once, stages day+note through the planner) and build_req_capture_jump(bob_dir, batch, target, owners, plan) -> (CaptureJumpJson, ReqLanding); task-offer pins return None and keep jump::build_capture_jump. Required per-item order on every managed Done path: tree close -> ordinary plan_successors staged -> plan_req_write_pass -> plan_req_link_pass with closing = closing_after_successors(&closing, &successor_plan) (None for !) -> ledger retirement. successors.rs gained SuccessorPlan.closing_continuation, DayView::anchor_for_owner, route_created_successor (shared D7 routing). req_writes now accepts open reqs under the just-closed owner (derived Met) and scopes rows to the frozen owner; ReqWriteOutcome.source_line added. Fixture: RV29-RV35 placement, RV36-RV43 jump (README documents shapes). Drop the cfg_attr(not(test), allow(dead_code)) on task_complete::{req_landing, req_placement} and capture::req_placement when wiring.

[2026-11-22T16:08:19Z · bob-cli-on.8.1.4] PROPOSED FOLLOW-UP: req_verdicts overlap/fold ancestry skips hand-ticked intermediates — validate_non_overlapping and ReqChoiceState::fold walk parent_key only through Pending card rows, so an ancestor Drop/Carry plus an explicit descendant verdict separated by a hand-ticked [x] row is not refused as req_verdict_overlap (the write pass then refuses as req_close_stale instead) and the descendant is not folded; walk ReqCloseOwner.nodes ancestry as req_landing now does, and add an RV choices case.

[2026-11-22T16:08:26Z · bob-cli-on.8.1.4] Placement and jump landed: carry_pulled tasks link once at the owner ordinary successor destination (slot, inherit, closing continuation reusing any placeholder the ordinary successors created, implicit fallback, shared D7 routing), raised to Next with no fresh/unblocked/keeps stamp; carry without pull-in stays unlinked; no destination refuses the batch. Pinned requirement landings resolve after all writes/routes by exact identity (created block, move-map-checked descendant line, owner-scoped path+text), forwarding inbox-route moves/renames; lost/ambiguous pins refuse. Fixed a phase-3 gap: writes now run on the post-close snapshot and never take another owner row. Verified: RV29-RV43 vectors, 18 placement/jump/adapter tests, post-close write tests; just check exit 0 (fmt, clippy gate, 12672 passed / 0 failed) on base d5e31abc plus this change; no epic symbols.

## Dependencies

- **Depends on:** [bob-cli-on.8.1.3](bob-cli-on.8.1.3.md) ✓ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-on.8.1.5](bob-cli-on.8.1.5.md) ◐ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.8.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.8.1.4/README.md) | [bob-cli-on.8.1.4](bob-cli-on.8.1.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`bddf386`](https://github.com/bobs-org/bob-cli/commit/bddf3868bf341287df9a5b8f0e1d5e931ac2155e) | feat(task-complete): place pulled requirement carries and resolve req jump landings | [bob-cli-on.8.1.4](bob-cli-on.8.1.4.md) | 2026-11-22 11:09:26 EST |
