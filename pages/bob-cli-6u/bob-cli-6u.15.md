# Bead: bob-cli-6u.15 — Fix the cycler and block-id-prompt for the line model

[Bead Pages](../README.md) / [bob-cli-6u](README.md) / bob-cli-6u.15

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.70](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.70.md) · **Assignee:** `bob-cli-6u.15` · **Size:** medium
**Created:** 2026-10-12 10:26:02 EDT · **Closed:** 2026-10-12 12:15:18 EDT
**Plan:** [202610/prj\_line\_project\_blocking.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prj_line_project_blocking.md)

## Description

plugins-compat: 3208e8c follow-up: read ^prj inline scheduled, use the resident tag as the project-blocked signal, write tag strips and [unblocked::] on recovery, refuse linking a date-blocked ^prj, drop the whole-vault read.

## Notes

[2026-10-12T14:45:48Z · 72] COORDINATION — bob-cli-6t.3 (running) adds task-status-cycler fragment 088-successor-project.js (projectDrainState, removeProjectHideTags, planProjectPullIns). It edits 085-successor-plan.js (relaxed gate, one row per R, breaker exemption, trigger/hide_removed) and plans a 137-plugin-successor-project.js mixin and 136 receipt changes. It reuses projectDependencyInfo/projectIsBlockedAfter (080) for its step 3. When you move those helpers to the inline ^prj date and the #prj_is_blocked signal, update 6t.3's callers too, and include its recover-rank writes (? → space) in your [unblocked::] rewrite. 085's headroom is shared, so avoid its fragment numbers. See research:202610/bob_cli_6t_6u_epic_conflict.md.

[2026-10-12T16:15:10Z · bob-cli-6u.15] PROPOSED FOLLOW-UP: Fix seven clean-base bob-plugins test failures — four unblocked-glyph tests, the Keep-count notice test, and two scheduled-roll status tests fail identically at clean HEAD.

[2026-10-12T16:15:18Z · bob-cli-6u.15] Project-blocking plugins built; phase suites pass; npm run validate passes; bob plugins sync succeeded. Full npm test: 2466/2473 passed; the seven remaining failures reproduce unchanged on clean HEAD and are recorded as a proposed follow-up.

## Dependencies

- **Depends on:** [bob-cli-6u.1](bob-cli-6u.1.md) ✓ · ⧖ 2026-10-12
- **Depends on:** [bob-cli-6u.10](bob-cli-6u.10.md) ✓ · ⧖ 2026-10-12
- **Blocks:** [bob-cli-6u.16](bob-cli-6u.16.md) ◐ · ⧖ 2026-10-12
- **Blocks:** [bob-cli-6u.17](bob-cli-6u.17.md) ◐ · ⧖ 2026-10-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6u.15](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.15/README.md) | [bob-cli-6u.15](bob-cli-6u.15.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@744247c`](https://github.com/bobs-org/bob-plugins/commit/744247ceee0f22279f0a9754470e2ff4957b4f5e) | feat(project-blocking): align cycler and block-id handling | [bob-cli-6u.15](bob-cli-6u.15.md) | 2026-10-12 12:16:22 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:72][1] | Assess 6u phase state and deps for conflict analysis with 6t | 1 |
| read-by | [agent:bob-cli-6u.8][2] | Need epic and children status | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.72/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.8/README.md

<!-- sase:referenced-by:end -->
