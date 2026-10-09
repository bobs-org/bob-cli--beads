# Bead: bob-cli-5w.8 — Recover-and-link on every Ctrl+Enter close, with one notice

[Bead Pages](../README.md) / [bob-cli-5w](README.md) / bob-cli-5w.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.0p.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.0p.linker.w0.md) · **Assignee:** `bob-cli-5w.8` · **Size:** medium
**Created:** 2026-10-09 11:54:15 EDT · **Closed:** 2026-10-09 13:15:57 EDT
**Plan:** [202610/successor\_links.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/successor_links.md)

## Description

cycler_wiring: in task-status-cycler, run the gated recover-and-link pass inside finalizeClosedTasks, with a closing-entry hint from Pomodoro-line closes. Write through open editors or through preimage-checked vault.process. Show the nav card, or compose the text into the walk toast and nav's completeTaskAtCursor caller, and report failures. Ships guard tests, version bumps, a README update, and a sync.

## Notes

[2026-10-09T17:15:24Z · bob-cli-5w.8] PROPOSED FOLLOW-UP: record decisions strand closed-task-hands-slot-to-successors per epic closeout memory decision (decision_record=no, deferred to land agent)

[2026-10-09T17:15:30Z · bob-cli-5w.8] PROPOSED FOLLOW-UP: add glossary strand successor-link cross-linked to task-link per epic closeout memory decision (glossary_term=no, deferred to land agent)

[2026-10-09T17:15:37Z · bob-cli-5w.8] PROPOSED FOLLOW-UP: give legacy recoverBlockedDependentsNow the Warm Tasks-cache index so warm closes skip the vault-wide scan (successor pass already reads only candidate notes + daily; legacy still full-scans as backstop)

[2026-10-09T17:15:42Z · bob-cli-5w.8] PROPOSED FOLLOW-UP: test-navigation-roll-decay has 2 date-sensitive failures (picker-single P2 roll cases) that fail identically on the clean base tree; already tracked by bob-cli-5w.6 note #3 and bob-cli-5w.7 note #1

[2026-10-09T17:15:48Z · bob-cli-5w.8] PROPOSED FOLLOW-UP: stage-ranker 1000-task 16ms threshold flakes under full-suite load (14/14 green in isolation x3, untouched code paths); consider raising budget or splitting the perf assertion

[2026-10-09T17:15:57Z · bob-cli-5w.8] cycler_wiring landed in bob-plugins: new 135-plugin-successors fragment (gated recover-and-link in finalizeClosedTasks, Pomodoro closing-entry hint with headline re-location, editor/vault-preimage writes, nav-card/walk-toast/plain-notice reporting), completeTaskAtCursor successorNotice + nav 535 toast composition; 10/10 new guard tests, focused 146/146, full suite 2318/2321 (2 pre-existing roll-decay fails identical on clean tree + 1 load-flaky ranker); cycler 1.28.0, nav 2.15.1, README rows updated, bob plugins sync deployed; epic-symbols clean

## Dependencies

- **Blocks:** [bob-cli-5w.10](bob-cli-5w.10.md) ◐ · ⧖ 2026-10-09
- **Depends on:** [bob-cli-5w.6](bob-cli-5w.6.md) ✓ · ⧖ 2026-10-09
- **Depends on:** [bob-cli-5w.7](bob-cli-5w.7.md) ✓ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-5w.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5w.8/README.md) | [bob-cli-5w.8](bob-cli-5w.8.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@e8b3584`](https://github.com/bobs-org/bob-plugins/commit/e8b3584bdb1144c82f84a6f0da74d96d9a8de6fb) | feat(task-status-cycler): recover-and-link successors on every Ctrl+Enter close with one notice | [bob-cli-5w.8](bob-cli-5w.8.md) | 2026-10-09 13:18:35 EDT |
