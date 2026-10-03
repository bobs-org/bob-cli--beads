# Bead: bob-cli-3n.12.9.3 — Finish the hand-edit mirror baseline and the Depends on stage

[Bead Pages](../README.md) / [bob-cli-3n.12.9](bob-cli-3n.12.9.md) / bob-cli-3n.12.9.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-3n.12.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-3n.12.land.md) · **Assignee:** `bob-cli-3n.12.9.3` · **Size:** medium
**Created:** 2026-10-03 01:27:48 EDT · **Closed:** 2026-10-03 02:03:44 EDT
**Plan:** [202610/task\_dep\_links\_landing\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_dep_links_landing_fixes.md)

## Description

nav-mirror-stage: seed the mirror from the CM6 start state and map the owner through later changes, delete the dead scheduleDependencyHandEditMirror path, count only open prerequisites in the waits-on badge, show readable cycle tooltips, reopen on every stale refusal, and add the missing stage harness tests.

## Notes

[2026-10-03T06:03:44Z · bob-cli-3n.12.9.3] nav-mirror-stage done in bob-plugins (nav 1.61.0): mirror baseline seeds from first CM6 startState with owner mapped via mapPos; dead scheduleDependencyHandEditMirror deleted; waits-on badge counts open prereqs (builder openCount, DC7/DC8); cycle tooltips show descriptions (dependent text wired through builder); stale refusals in 3 confirm fns + same-note batch skips route through refuseDependencyStale with reopen (plugin-level pendingTargetLine guard left as-is: unreachable defensive TOCTOU, no stage to reopen). Tests: 3 new mirror listener tests + 10 new stage harness tests; npm test 1350/1350 pass, npm run validate 6/6, deployed via bob plugins sync (2 copied). Changes uncommitted in linked bob-plugins checkout for the land agent; bob-cli tree untouched.

## Dependencies

- **Depends on:** [bob-cli-3n.12.9.2](bob-cli-3n.12.9.2.md) ✓ · ⧖ 2026-10-03
- **Blocks:** [bob-cli-3n.12.9.5](bob-cli-3n.12.9.5.md) ✓ · ⧖ 2026-10-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3n.12.9.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3n.12.9.3/README.md) | [bob-cli-3n.12.9.3](bob-cli-3n.12.9.3.md) | 0 |
