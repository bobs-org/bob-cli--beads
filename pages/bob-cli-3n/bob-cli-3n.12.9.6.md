# Bead: bob-cli-3n.12.9.6 — Finish the task dependency landing fixes: nav regressions, mirror owner, stage badge, DP30 chips, Reading-view line, R9 hooks, rollout

[Bead Pages](../README.md) / [bob-cli-3n.12.9](bob-cli-3n.12.9.md) / bob-cli-3n.12.9.6

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-3n.12.9.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-3n.12.9.land.md) · **Assignee:** `bob-cli-3n.12.9.6.land`
**Created:** 2026-10-03 02:54:24 EDT
**Plan:** [202610/task\_dep\_links\_landing\_remaining.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_dep_links_landing_remaining.md)

## Description

Every gap and regression the bob-cli-3n.12.9 landing audit confirmed is fixed and pinned by a test that fails on the pre-fix source: nav recovers, refuses, and commits correctly on every writer path; the mirror edits the right task; the stage never shows "waits on 0"; chips render on DP30 and act on the right Reading-view row; the hooks apply R9 to label-only lines; and the fixed bob and plugins are installed across the fleet.

## Notes

[2026-10-03T08:33:53Z · bob-cli-3n.12.9.6.land] Land follow-up triage: the only PROPOSED FOLLOW-UP (bob-cli-3n.12.9.6.3, the capture_pomodoros missing_note_and_missing_section_are_warning_successes env-race flake) duplicates bob-cli-2e. I gave it a +1 with my own repro on 50350db (1 fail in a parallel lib run, passes alone); no new task. Landing audit found epic-caused gaps that remain epic work: (1) a doubled 'changed — reopen' notice when a stage write goes stale, because applyDependencyEdit and refuseDependencyStale both notify; (2) removeCountedDependency still shows 'Selected dependency changed' instead of calling refuseDependencyStale; (3) comments still describe per-source writes and skipped stale rows; (4) no test checks the changed-only N in the counted notices; (5) the subfolder writer test stubs readDependencyVaultFileList and dependencyLinkpathResolver; (6) stage tests do not use the picker harnesses, and the cycle test uses a hand-built batch whose rows are each already a cycle; (7) the counted local add path reads the vault snapshot for any [?] source even on an add; (8) contract §7.4 still excludes Reading rows under Work Log entries (contradicts DP30) and does not describe order-mapped rows; (9) DP30 Reading row actions are untested; (10) nav comments cite §6.4 for the badge rule, which lives in §6.3; (11) an unreachable legacy.is_empty() branch remains in reconcile.rs plan_adoption. Also accepted, not changed: 94131c7's write_dependent_field helper now reports the R2 keep-path field rewrite as a dependent_field update, which was silent before. This matches contract §4.3 ('Report every change'). A tale plan finishes these and closes the epic.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3n.12.9.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-3n.12.9.6.land.md) | [bob-cli-3n.12.9.6](bob-cli-3n.12.9.6.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@5d6e769`](https://github.com/bobs-org/bob-plugins/commit/5d6e7690c05edc63c90bde4a9db283335c2fef8f) | fix(nav): single stale notice, counted snapshot gate, real-path stage tests (1.64.0) | [bob-cli-3n.12.9.6](bob-cli-3n.12.9.6.md) | 2026-10-03 04:52:23 EDT |
| bob-cli | [`6192017`](https://github.com/bobs-org/bob-cli/commit/619201720934e641db800d7d2e86a8f6ac714193) | docs(task-deps): DP30 Reading rows in 7.4; drop unreachable legacy branch | [bob-cli-3n.12.9.6](bob-cli-3n.12.9.6.md) | 2026-10-03 04:52:53 EDT |
