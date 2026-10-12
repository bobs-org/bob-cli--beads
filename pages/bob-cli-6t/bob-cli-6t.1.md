# Bead: bob-cli-6t.1 — Project pull-in contract and PP vectors

[Bead Pages](../README.md) / [bob-cli-6t](README.md) / bob-cli-6t.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.6z](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.6z.md) · **Assignee:** `bob-cli-6t.1` · **Size:** small
**Created:** 2026-10-12 10:07:29 EDT · **Closed:** 2026-10-12 10:23:30 EDT
**Plan:** [202610/project\_task\_pull\_in.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/project_task_pull_in.md)

## Description

contract: add docs/task-dependencies.md §12.10 (trigger, rule, gate, writes, reporting, copy, undo, interplay) with PP vectors, and amend §12, §13.4, projects/plan/capture docs, and README.

## Notes

[2026-10-12T14:17:34Z · bob-cli-6t.1] PROPOSED FOLLOW-UP: skipped decisions-web record project-pull-in-on-empty — decision_record=no; add a strand claiming a close that empties a project links ^prj as Next and drops #hide, using sync's predicate, with links to task-lanes-are-sticky and project-deps-block-resident-tasks if that record exists.

[2026-10-12T14:23:23Z · bob-cli-6t.1] PROPOSED FOLLOW-UP: just all / cargo test --test cli percent_listen fails identically on the clean base tree (failed_percent_listen_worker_keeps_listen_retry_guidance, percent_listen_reference_runs_existing_worker_and_installs_audio) — already tracked by bob-cli-6m.

[2026-10-12T14:23:30Z · bob-cli-6t.1] Added docs/task-dependencies.md §12.10 (trigger a/b, rule, gate, writes, reporting, undo, interplay) and §12.11 PP1–PP24; amended §12, SL11, PDC2, §13.4, plus projects/plan/capture/README pointers. unblocked_prj=yes, subproject_cascade=no, decision_record skipped as a PROPOSED FOLLOW-UP. just all: fmt and clippy passed; the two capture percent_listen CLI failures reproduce on the clean base tree and are tracked by bob-cli-6m. No leftover --epic-symbol entries.

## Dependencies

- **Blocks:** [bob-cli-6t.2](bob-cli-6t.2.md) ◐ · ⧖ 2026-10-12
- **Blocks:** [bob-cli-6t.3](bob-cli-6t.3.md) ◐ · ⧖ 2026-10-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6t.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6t.1/README.md) | [bob-cli-6t.1](bob-cli-6t.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ec7251e`](https://github.com/bobs-org/bob-cli/commit/ec7251eb91b478f761e9de0bb394b8f3393ecba3) | docs(task-dependencies): add project pull-in contract and PP vectors | [bob-cli-6t.1](bob-cli-6t.1.md) | 2026-10-12 10:24:44 EDT |
