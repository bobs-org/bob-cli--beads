# Bead: bob-cli-e6.7 — Bare captures place links by task type

[Bead Pages](../README.md) / [bob-cli-e6](README.md) / bob-cli-e6.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2t.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2t.linker.w0.md) · **Assignee:** `bob-cli-e6.7` · **Size:** medium
**Created:** 2026-10-29 16:16:34 EDT · **Closed:** 2026-10-29 23:27:39 EDT
**Plan:** [202610/task\_types.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_types.md)

## Description

capture-placement: route every bare link-creating capture form to the Pomodoro chosen by the task's effective type, report it additively in JSON and previews, and refuse under plan.strict.

## Notes

[2026-10-30T03:17:11Z · bob-cli-e6.7] PROPOSED FOLLOW-UP: ref-today/capture parity test today_matches_unnamed_capture_and_named_capture_remembers_theme is red between phases — capture now places bare links by type (this phase) while `bob ref today` still passes None and uses the legacy implicit entry; route to bob-cli-e6.12, which wires typed placement into link_existing_task and restores parity (both sides then run place())

[2026-10-30T03:17:22Z · bob-cli-e6.7] PROPOSED FOLLOW-UP: lib test capture_related archive_closed_window_respects_mtime fails identically on the clean base tree, verified via stash with and without this phase changes. Pre-existing mtime failure in unrelated capture-related archive code; needs a task bead and owner outside this phase

[2026-10-30T03:27:39Z · bob-cli-e6.7] Bare captures place links by type: shared select_typed_implicit_entry in capture_task_toggle wired into whole-item links, new-task links, project-note per-task links, toggle, Ensure Next, and bare link-starts; additive type object on destinations plus human suffix; strict_cap refusal with teaching message. Verified: 10 new CLI acceptance tests in typed_placement.rs and 6 new pure planner unit tests pass; 143-test focused sweep incl. pomodoro_link/task_toggle/ensure_next/project_note/start/plan_budget/task_theme_writes/docs_reference green; 70 lib planner tests green; fmt clean; clippy gate 0 errors; docs-check passed. Two intentional deviations recorded: created-row keeps pinned order as arrow-new-Pomodoro-X plus suffix, and pure task-less = keeps legacy rule. Two PROPOSED FOLLOW-UP notes on bead: ref-today parity seam owned by e6.12, and pre-existing base-tree mtime failure. Protocol.md edits live only in the gitignored sidecar mount; durable Mac copy belongs to e6.15 lane.

## Dependencies

- **Blocks:** [bob-cli-e6.12](bob-cli-e6.12.md) ○ · ⧖ 2026-10-29
- **Blocks:** [bob-cli-e6.14](bob-cli-e6.14.md) ◐ · ⧖ 2026-10-29
- **Blocks:** [bob-cli-e6.15](bob-cli-e6.15.md) ✓ · ⧖ 2026-10-29
- **Depends on:** [bob-cli-e6.6](bob-cli-e6.6.md) ✓ · ⧖ 2026-10-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-e6.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-e6.7/README.md) | [bob-cli-e6.7](bob-cli-e6.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`1ba6437`](https://github.com/bobs-org/bob-cli/commit/1ba6437a8e813ca2f0fbbf9245237d97f384622b) | feat(capture): bare captures place links by task type | [bob-cli-e6.7](bob-cli-e6.7.md) | 2026-10-29 23:29:46 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-e6.7][1] | Verify follow-up notes landed before final verification | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-e6.7/README.md

<!-- sase:referenced-by:end -->
