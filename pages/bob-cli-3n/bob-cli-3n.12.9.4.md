# Bead: bob-cli-3n.12.9.4 — Close the hooks DW, DP, Summary, docs, and per-run copy gaps

[Bead Pages](../README.md) / [bob-cli-3n.12.9](bob-cli-3n.12.9.md) / bob-cli-3n.12.9.4

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-3n.12.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-3n.12.land.md) · **Assignee:** `bob-cli-3n.12.9.4` · **Size:** medium
**Created:** 2026-10-03 01:27:48 EDT
**Plan:** [202610/task\_dep\_links\_landing\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_dep_links_landing_fixes.md)

## Description

hooks-gaps: replace the hollow DW1/DW2/DW3/DW5/DW6 tests, pin the Summary dependency counts, fix the task-status-hooks JSON example, narrow a needless pub(crate), and stop ReconcileWorker::new copying every vault note per run.

## Notes

[2026-10-03T05:53:05Z · bob-cli-3n.12.9.4] Real-vault dry-run wall time (~/bob, 4636 notes, BOB_DAY_FILE=2026/20261002.md): before 10385/10445/10915ms (mean ~10.6s), after 10836/10790/10859ms warm (mean ~10.8s); delta +2% is inside run-to-run variance (before-range alone spans 530ms). Dry-run JSON reports byte-identical before/after. Reconcile line-view work is a small share of the pass; the win is allocation-side (no owned per-line copy for notes without tasks or block ids, one line-view pass per note).

[2026-10-03T05:53:09Z · bob-cli-3n.12.9.4] PROPOSED FOLLOW-UP: completion::bash::bash_readline_inserts_what_bob_returned flakes under parallel cargo test (fails in full run, passes in isolation); needs quarantine or retry like the capture_pomodoros flake (bob-cli-2e)

## Dependencies

- **Blocks:** [bob-cli-3n.12.9.5](bob-cli-3n.12.9.5.md) ◐ · ⧖ 2026-10-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3n.12.9.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3n.12.9.4/README.md) | [bob-cli-3n.12.9.4](bob-cli-3n.12.9.4.md) | 0 |
