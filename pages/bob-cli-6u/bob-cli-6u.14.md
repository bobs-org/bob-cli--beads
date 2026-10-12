# Bead: bob-cli-6u.14 — Project conversion and task moves on the line model

[Bead Pages](../README.md) / [bob-cli-6u](README.md) / bob-cli-6u.14

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.70](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.70.md) · **Assignee:** `bob-cli-6u.14` · **Size:** medium
**Created:** 2026-10-12 10:26:02 EDT · **Closed:** 2026-10-12 16:03:00 EDT
**Plan:** [202610/prj\_line\_project\_blocking.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prj_line_project_blocking.md)

## Description

nav-convert-move: create-project-note-from-task keeps the Depends-On line and inline date on ^prj both ways (accepts [?], rebases links, skips Sub-projects); Ctrl+Shift+M into or out of a blocked project tags or recovers.

## Notes

[2026-10-12T20:00:29Z · bob-cli-6u.14] PROPOSED FOLLOW-UP: Fix five clean-base bob-plugins test failures — test-ledger-tools-unblocked-glyph.cjs has four failing glyph-rendering cases and test-navigation-decision-card-handlers.cjs has one Keep-count notice failure; all five reproduce with the committed navigation-hotkeys bundle, and no existing bead matched these failures.

[2026-10-12T20:03:00Z · bob-cli-6u.14] Built and synced bob-navigation-hotkeys 2.24.0. Focused conversion, reversal, task-move, and schedule-recovery tests pass (92/92); npm run validate passes. Full npm test has five failures reproduced with the committed HEAD bundle (four unblocked-glyph cases and one Keep-count notice); recorded as a PROPOSED FOLLOW-UP. epic-symbols reports no leftovers.

## Dependencies

- **Depends on:** [bob-cli-6u.13](bob-cli-6u.13.md) ✓ · ⧖ 2026-10-12
- **Blocks:** [bob-cli-6u.16](bob-cli-6u.16.md) ◐ · ⧖ 2026-10-12
- **Blocks:** [bob-cli-6u.17](bob-cli-6u.17.md) ✓ · ⧖ 2026-10-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6u.14](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.14/README.md) | [bob-cli-6u.14](bob-cli-6u.14.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e9acfdf`](https://github.com/bobs-org/bob-cli/commit/e9acfdf7264098425e6176ecb6b65afeeda7487a) | docs(projects): document line-based conversion behavior | [bob-cli-6u.14](bob-cli-6u.14.md) | 2026-10-12 16:04:13 EDT |
| bob-plugins | [`bob-plugins@1abde2f`](https://github.com/bobs-org/bob-plugins/commit/1abde2f639ff709dea6db6e36a90ee5c6a4962c2) | feat(navigation): preserve project state across conversion and moves | [bob-cli-6u.14](bob-cli-6u.14.md) | 2026-10-12 16:05:32 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:72][1] | Assess 6u phase state and deps for conflict analysis with 6t | 1 |
| read-by | [agent:bob-cli-6u.14][2] | Check whether earlier work left remaining phase notes | 2 |
| read-by | [agent:bob-cli-6u.8][3] | Need epic and children status | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.72/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.14/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.8/README.md

<!-- sase:referenced-by:end -->
