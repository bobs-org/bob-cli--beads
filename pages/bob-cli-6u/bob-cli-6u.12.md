# Bead: bob-cli-6u.12 — ^prj Schedule uses the inline path with project side effects

[Bead Pages](../README.md) / [bob-cli-6u](README.md) / bob-cli-6u.12

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase · **↺ Reopened:** ↺1
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.70](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.70.md) · **Assignee:** `bob-cli-6u.12` · **Size:** medium
**Created:** 2026-10-12 10:26:02 EDT · **Closed:** 2026-10-12 14:24:33 EDT
**Plan:** [202610/prj\_line\_project\_blocking.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prj_line_project_blocking.md)

## Previously Closed

> ↺ Closed 2026-10-12T17:13:23Z · done
>
> (none)
>
> Reopened 2026-10-12T17:24:05Z by a status update

## Description

nav-schedule: retire project-frontmatter routing for scheduled, stop stripping inline ^prj dates, keep propagation (plus the move-earlier fix) and #hide, block or recover residents, child-picker chip from ^prj.

## Notes

[2026-10-12T17:13:08Z · bob-cli-6u.12] PROPOSED FOLLOW-UP: Baseline plugin tests still fail on the clean tree — 4 scripts/test-ledger-tools-unblocked-glyph.cjs cases (Live Preview glyph, widget mousedown, rebuild triggers, Reading view) plus scripts/test-navigation-decision-card-handlers.cjs Keep counts once (notice is "Update Bob Ledger Tools to record review stats")

[2026-10-12T17:13:23Z · bob-cli-6u.12] nav-schedule: retired project-frontmatter routing; ^prj scheduled is inline with raise-only plus move-earlier replaceExact, #hide, #prj_is_blocked on remaining future residents, [unblocked::] on other-line Ready recoveries, and Pomodoro consume with removeEmptiedEntries. Child-note calendar-clock chip reads ^prj from a warm Tasks cache. Picker roll/date writes pass the picker today. Plugin 2.22.0 built, validated, deployed on this host (bob plugins sync -n -p bob-navigation-hotkeys). docs/projects.md Task Card / Scheduling / child chip updated. npm test 2489 pass / 5 fail identical to clean tree (unblocked-glyph + decision-card Keep notice). epic-symbols: none. Did not close parent epic bob-cli-6u.

[2026-10-12T17:24:05Z · bryanbugyi34@gmail.com] I think this work might be completed but the agent failed so I'm not sure.

[2026-10-12T18:23:52Z · bob-cli-6u.12] PROPOSED FOLLOW-UP: Fix ledger-tools unblocked-glyph UI assertions — four failures remain in scripts/test-ledger-tools-unblocked-glyph.cjs (Live Preview placement, widget cursor placement, rebuild refresh, and Reading view rendering); the ledger-tools source and tests were untouched by this phase, and no matching task bead was found.

[2026-10-12T18:23:57Z · bob-cli-6u.12] PROPOSED FOLLOW-UP: Fix the Keep decision-card notice assertion — scripts/test-navigation-decision-card-handlers.cjs expects a Keep-count notice but receives the Bob Ledger Tools stats-version notice; the handler and test were untouched by this phase, and no matching task bead was found.

[2026-10-12T18:24:03Z · bob-cli-6u.12] PROPOSED FOLLOW-UP: bob-cli-3w tracks the stage-ranker 16 ms budget flake — it failed under full npm test load at 44.7 ms and passed when run alone.

[2026-10-12T18:24:33Z · bob-cli-6u.12] Implemented and deployed inline ^prj schedule routing, propagation/move-earlier, tagged blocking and recovery with Pomodoro cleanup, and inline child-note schedule badges. Verified build, targeted suites (60/60 and roll/review 71/71), and validation (6/6 manifests). Full npm test reported 2487/2493 passing; the six residual failures are recorded as follow-up notes, including the stage-ranker load flake linked to bob-cli-3w.

## Dependencies

- **Depends on:** [bob-cli-6u.11](bob-cli-6u.11.md) ✓ · ⧖ 2026-10-12
- **Blocks:** [bob-cli-6u.13](bob-cli-6u.13.md) ◐ · ⧖ 2026-10-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6u.12](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.12/README.md) | [bob-cli-6u.12](bob-cli-6u.12.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e7dee5d`](https://github.com/bobs-org/bob-cli/commit/e7dee5ddd23ccf16b38439e8597bbf9670c4696b) | docs(projects): document inline project scheduling | [bob-cli-6u.12](bob-cli-6u.12.md) | 2026-10-12 14:25:48 EDT |
| bob-plugins | [`bob-plugins@a42f45d`](https://github.com/bobs-org/bob-plugins/commit/a42f45d6e32089daf77235913a8d20f926d0d616) | feat(navigation): schedule projects from inline ^prj fields | [bob-cli-6u.12](bob-cli-6u.12.md) | 2026-10-12 14:27:14 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:72][1] | Assess 6u phase state and deps for conflict analysis with 6t | 1 |
| read-by | [agent:bob-cli-6u.8][2] | Need epic and children status | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.72/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.8/README.md

<!-- sase:referenced-by:end -->
