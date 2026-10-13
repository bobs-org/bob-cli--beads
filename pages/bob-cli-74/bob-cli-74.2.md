# Bead: bob-cli-74.2 — Shared sync surface predicate and the Rust pull-in planner

[Bead Pages](../README.md) / [bob-cli-74](README.md) / bob-cli-74.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.73](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.73.md) · **Assignee:** `bob-cli-74.2` · **Size:** medium
**Created:** 2026-10-12 23:40:11 EDT · **Closed:** 2026-10-13 00:33:19 EDT
**Plan:** [202610/project\_pull\_in\_line\_model.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/project_pull_in_line_model.md)

## Description

cli-model: factor sync's surface predicate into one crate-visible projects helper, widen normalize_task_hide_tag, add the pure task_complete/project_pull_in.rs planner, wire it into plan_successors (gate, merge, breaker, #hide edit, [unblocked::], cascade, row fields), and pin the planner-level PP vectors.

## Notes

[2026-10-13T04:33:09Z · bob-cli-74.2] PROPOSED FOLLOW-UP: Add decisions-web record project-pull-in-on-empty for the project pull-in rule (skipped per epic decision_record=no; cf. bob-cli-74.1 note #1)

[2026-10-13T04:33:19Z · bob-cli-74.2] cli-model done: projects/surface.rs shares sync predicate (factored effective_unhidden_count/should_surface_project, sync tests untouched); normalize_task_hide_tag pub(crate); task_complete/project_pull_in.rs planner wired into plan_successors (gate, merge, breaker-exempt, hide-strip before unblock scope, trigger/hide_removed rows, [?]-gated cascade); 30 planner PP tests (PP1-PP15,PP17,PP20,PP22,PP24-PP28+gate) + 8 sync/surface agreement tests green; lib 2492/2492 green; just check otherwise green except the 2 plan-allowed bob-cli-6m percent-listen failures also seen by docs-only 74.1; one stale SL test updated to already_planned per the specified project_task replacement; epic-symbols clean; callers compile with empty note_texts for cli-capture

## Dependencies

- **Depends on:** [bob-cli-74.1](bob-cli-74.1.md) ✓ · ⧖ 2026-10-12
- **Blocks:** [bob-cli-74.3](bob-cli-74.3.md) ◐ · ⧖ 2026-10-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-74.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-74.2/README.md) | [bob-cli-74.2](bob-cli-74.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`5fc27f0`](https://github.com/bobs-org/bob-cli/commit/5fc27f0818e7b677b3da3bff23253b0f0c5a8387) | feat(pull-in): shared sync surface predicate and Rust pull-in planner | [bob-cli-74.2](bob-cli-74.2.md) | 2026-10-13 00:34:48 EDT |
