# Bead: bob-cli-74.5 — Render pull-in and project rows in nav's Unblocked card

[Bead Pages](../README.md) / [bob-cli-74](README.md) / bob-cli-74.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.73](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.73.md) · **Assignee:** `bob-cli-74.5` · **Size:** small
**Created:** 2026-10-12 23:40:12 EDT · **Closed:** 2026-10-12 23:56:31 EDT
**Plan:** [202610/project\_pull\_in\_line\_model.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/project_pull_in_line_model.md)

## Description

nav: in 285-unblocked-notice.js add the no-open-tasks chip, the Project empty title, the still-blocked pull-in suffix, the project member label and blocked-by-project copy (also for legacy project_dependency/project_schedule reasons), mirror the fallback text, test, bump, and deploy on this host.

## Notes

[2026-10-13T03:55:56Z · bob-cli-74.5] PROPOSED FOLLOW-UP: Add the project-pull-in-on-empty decisions-web record — epic decision_record was false, so this phase intentionally did not edit memory.

[2026-10-13T03:56:04Z · bob-cli-74.5] PROPOSED FOLLOW-UP: Fix five bob-plugins npm test failures — scripts/test-ledger-tools-unblocked-glyph.cjs has four failures and scripts/test-navigation-decision-card-handlers.cjs has one; all reproduced on clean base 5d8975b.

[2026-10-13T03:56:31Z · bob-cli-74.5] Implemented nav project-empty and project-blocked row labels/copy, fallback strings, tests, manifest 2.28.0; npm run build, focused notice tests (17/17), npm run validate, deploy, and epic-symbol check verified. npm test has five failures reproduced unchanged at clean base 5d8975b; follow-ups recorded on bead.

## Dependencies

- **Depends on:** [bob-cli-74.1](bob-cli-74.1.md) ✓ · ⧖ 2026-10-12
- **Blocks:** [bob-cli-74.6](bob-cli-74.6.md) ◐ · ⧖ 2026-10-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-74.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-74.5/README.md) | [bob-cli-74.5](bob-cli-74.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@00f3e8f`](https://github.com/bobs-org/bob-plugins/commit/00f3e8f7495a457d2c2c8681234fb034cabd2480) | feat(navigation): render project pull-in notices | [bob-cli-74.5](bob-cli-74.5.md) | 2026-10-12 23:57:08 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-74.5][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-74.5/README.md

<!-- sase:referenced-by:end -->
