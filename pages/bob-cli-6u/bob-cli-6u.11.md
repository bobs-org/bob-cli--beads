# Bead: bob-cli-6u.11 — Salvage the stranded nav-model work onto the ^prj line model

[Bead Pages](../README.md) / [bob-cli-6u](README.md) / bob-cli-6u.11

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.70](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.70.md) · **Assignee:** `bob-cli-6u.11` · **Size:** medium
**Created:** 2026-10-12 10:26:02 EDT · **Closed:** 2026-10-12 12:17:01 EDT
**Plan:** [202610/prj\_line\_project\_blocking.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prj_line_project_blocking.md)

## Description

nav-model: port the reusable parts of the uncommitted bob-cli-6s.8 bundle (project block state, recovery gate, ADJ-11, removeEmptiedEntries) to the ^prj line, add tag and [unblocked::] recovery writers, release as 2.21.0.

## Notes

[2026-10-12T14:45:43Z · 72] COORDINATION — bob-cli-6t.3 (project pull-in plugins phase, running) edits nav 285-unblocked-notice.js: project rows, a "Project empty" title, a project_member label, and "blocked by project" copy. Its plan bumps the nav manifest "from the latest master version" (2.19.0) and deploys nav on this host. A note on 6t.3 asks it to skip 2.20.0 and to leave the deploy until after your salvage. As of 10:45 EDT the deployed ~/bob/.obsidian/plugins/bob-navigation-hotkeys/manifest.json still says 2.20.0. Re-check before you start. If it was replaced, use the newest ~/.local/state/bob-cli/plugin-backups/<ts>/bob-navigation-hotkeys copy whose manifest says 2.20.0. If 6t.3's nav commit landed, rebase on it, merge 285 and the README/package.json rows, and bump from the higher version. See research:202610/bob_cli_6t_6u_epic_conflict.md.

[2026-10-12T16:16:53Z · bob-cli-6u.11] PROPOSED FOLLOW-UP: Triage the 20 bob-plugins npm test failures that also reproduce on the clean base (unblocked-glyph 4, keep-count 1, picker-single 2, successor-polish/wiring 12, stage-ranker flake 1; already recorded by bob-cli-6u.10 #1 citing bob-cli-6s.11 #1 and task bob-cli-3w).

[2026-10-12T16:17:01Z · bob-cli-6u.11] Ported 6s.8 nav project-blocking onto the ^prj line model as bob-navigation-hotkeys 2.21.0 (215 fragment, ADJ-11 walk-through, recovery gate, #prj_is_blocked/[unblocked::] writers, TICKLER unblocked copy, emptied-Pomodoro cleanup). YAML parseProjectDependsOn/planProjectDependsOnSplice gone from plugins/. New suite 18/18; related schedule-recovery/dependencies/deferred-pomodoro/freshness/unblocked-notice/plugin-build passed; npm run validate 6/6. Deployed to this host vault (manifest 2.21.0, setProjectBlockedTag present). epic-symbols empty. Full npm test still has the same 20 clean-base failures (19 date-frozen + stage-ranker flake); recorded follow-up citing bob-cli-6u.10 #1 / bob-cli-6s.11 #1 / bob-cli-3w.

## Dependencies

- **Depends on:** [bob-cli-6u.1](bob-cli-6u.1.md) ✓ · ⧖ 2026-10-12
- **Depends on:** [bob-cli-6u.10](bob-cli-6u.10.md) ✓ · ⧖ 2026-10-12
- **Blocks:** [bob-cli-6u.12](bob-cli-6u.12.md) ◐ · ⧖ 2026-10-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6u.11](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.11/README.md) | [bob-cli-6u.11](bob-cli-6u.11.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:72][1] | Assess 6u phase state and deps for conflict analysis with 6t | 1 |
| read-by | [agent:bob-cli-6u.11][2] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-6u.8][3] | Need epic and children status | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.72/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.11/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.8/README.md

<!-- sase:referenced-by:end -->
