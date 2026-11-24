# Bead: bob-cli-pl.5 — Report-backed lifecycle reasons, readouts, lint, and the ^prj goal line (bob-plugins)

[Bead Pages](../README.md) / [bob-cli-pl](README.md) / bob-cli-pl.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5y.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5y.linker.w1.md) · **Assignee:** `bob-cli-pl.5` · **Size:** medium
**Created:** 2026-11-22 20:56:40 EST · **Closed:** 2026-11-24 16:29:42 EST
**Plan:** [202611/area\_project\_cards.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/area_project_cards.md)

## Description

card-live: patch the cards in place from the already-cached areas/projects reports (blocked reasons, close dates, open/today readouts, contract issues in the foot lint) and decorate the recognized ^prj line as the note's goal.

## Notes

[2026-11-24T21:29:29Z · bob-cli-pl.5] PROPOSED FOLLOW-UP: Full test:unit shows 2 pre-existing perf-budget flakes (event-link-times 200-link build, frees-marks 200-link/2000-task build, both over the 25 ms budget); they fail identically on the clean base tree under full-suite load and pass in isolation, so they are environmental, not card-live regressions.

[2026-11-24T21:29:42Z · bob-cli-pl.5] card-live landed in bob-plugins: live patch (blocked reasons w/ max-2 links + nearest-ancestor walk, closed_on fill, open/today absent-not-zero, contract lint w/ first-setting =+ jump), ^prj goal-line decoration on Live Preview + Reading, 21 new unit tests, e2e fixtures/probe/checks for dep-blocked/sub-blocked/undated-done/goal, docs section. Verified: build:check, docs:check, 147/147 affected suites, full test:unit 9358/9365 with only the 2 pre-existing perf flakes (recorded as follow-up), bob plugins sync deployed.

## Dependencies

- **Depends on:** [bob-cli-pl.3](bob-cli-pl.3.md) ✓ · ⧖ 2026-11-22
- **Depends on:** [bob-cli-pl.4](bob-cli-pl.4.md) ✓ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-pl.9](bob-cli-pl.9.md) ◐ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pl.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pl.5/README.md) | [bob-cli-pl.5](bob-cli-pl.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@d59ee11`](https://github.com/bobs-org/bob-plugins/commit/d59ee11bd8621db6ca10b6826ffd5178604059e9) | feat(ledger-tools): add home card live patch with blocked-project links and goal line | [bob-cli-pl.5](bob-cli-pl.5.md) | 2026-11-24 16:31:04 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:fx][1] | Map the pl epic dependency graph | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.fx/README.md

<!-- sase:referenced-by:end -->
