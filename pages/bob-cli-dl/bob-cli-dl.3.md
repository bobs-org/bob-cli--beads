# Bead: bob-cli-dl.3 — Capture ~ / ~~ cancels the source in the same staged batch

[Bead Pages](../README.md) / [bob-cli-dl](README.md) / bob-cli-dl.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2r.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2r.linker.w0.md) · **Assignee:** `bob-cli-dl.3` · **Size:** medium
**Created:** 2026-10-28 08:15:27 EDT · **Closed:** 2026-10-28 11:26:09 EDT
**Plan:** [202610/relation\_cancel\_labels.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/relation_cancel_labels.md)

## Description

capture-cancel: on an Added or Relabeled relation with a cancel label, stage the source cancel, today's prune, and recovery in the capture batch with dry-run parity. Adds the new-task, recurring, and conflict refusals, relation_cancels[] and relation_updates[].cancel_effect JSON, the relation_cancelled_source structured warning, the human ⊘ row, and the capture docs.

## Notes

[2026-10-28T15:14:33Z · bob-cli-dl.3] PROPOSED FOLLOW-UP: base tree fails cargo check --tests (pomodoro_themes::Catalog cfg(test) for_suggest helper at src/native/pomodoro_themes/mod.rs:413 lacks the config_warning field); reproduces identically on clean HEAD worktree, so just check/clippy --all-targets and lib unit tests stay red until the themes owner fixes it

[2026-10-28T15:15:06Z · bob-cli-dl.3] PROPOSED FOLLOW-UP: rewriting a task line inside the ## Pomodoros section (open entry to [-]/[x] or any status flip) trips the PomodoroBlockTracker vanished-entry guard (debug builds panic exit 101, release silently misreports); reproduced with @day+daytask toggle and with a cancel-label source living in-section, so every status gesture shares it — needs an explicit block ref or a tracker carve-out

[2026-10-28T15:15:12Z · bob-cli-dl.3] PROPOSED FOLLOW-UP: plan_dependency_only_item never calls plan_relation_label_hides, so || one-off labels on @owner items are silently dropped (no relation_label_hides row, no journal event) while the same draft on the new-task form records them; the cancel still fires either way

[2026-10-28T15:26:09Z · bob-cli-dl.3] capture-cancel implemented and verified: collect/refuse/stage in src/native/capture/relations_cancel.rs (cancel-label Added/Relabeled edges deduped by source; coded refusals relation_cancels_new_task / relation_cancels_recurring_task / relation_cancel_conflicts_with_item_action; task_cancel plan staged through batch overlays with dry-run parity; relation_cancels[] + relation_updates[].cancel_effect + relation_cancelled_source warning + human ⊘ row once, warning JSON-only). 18 new CLI tests in tests/cli/capture/relations_cancel.rs cover forward/reverse cancel, prune, recovery with [unblocked::] stamp, all refusals, already-closed, rerun no-op, relabel in/away, two-edges-one-log, daily source/absent, mirror kill-switch, hidden + one-off labels, ^prj, still-blocked dependent, midnight dates, cross-item staged visibility, inert-without-config, invalid-config warning. Full cli suite 2346 passed; just docs-check passed; fmt clean; clippy gate flags clean on lib + cli targets. Known base breakage (lib unit-test target fails at HEAD from pomodoro_themes for_suggest missing config_warning; verified identical on clean worktree) and two discovered pre-existing gaps (in-section task rewrite vs block tracker; || hides dropped on @owner items) recorded as PROPOSED FOLLOW-UP notes.

## Dependencies

- **Depends on:** [bob-cli-dl.2](bob-cli-dl.2.md) ✓ · ⧖ 2026-10-28
- **Blocks:** [bob-cli-dl.7](bob-cli-dl.7.md) ◐ · ⧖ 2026-10-28
- **Blocks:** [bob-cli-dl.8](bob-cli-dl.8.md) ◐ · ⧖ 2026-10-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-dl.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-dl.3/README.md) | [bob-cli-dl.3](bob-cli-dl.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0a5f41b`](https://github.com/bobs-org/bob-cli/commit/0a5f41b8781a643071707a7534f667df6b932c6e) | feat(capture): cancel-label commits retire the source in the staged batch | [bob-cli-dl.3](bob-cli-dl.3.md) | 2026-10-28 11:27:23 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-dl.3][1] | Need the phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-dl.3/README.md

<!-- sase:referenced-by:end -->
