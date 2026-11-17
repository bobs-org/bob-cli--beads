# Bead: bob-cli-mu.1 — Album card field navigation on one painted order

[Bead Pages](../README.md) / [bob-cli-mu](README.md) / bob-cli-mu.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.57.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.57.linker.w0.md) · **Assignee:** `bob-cli-mu.1` · **Size:** medium
**Created:** 2026-11-17 15:36:25 EST · **Closed:** 2026-11-17 16:02:11 EST
**Plan:** [202611/schema\_card\_field\_jumps.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/schema_card_field_jumps.md)

## Description

field-nav: route the Schema Card's targets through one painted-order helper shared with the body painter, add Shift+J/K field steps and 1–9 field jumps with clamp-bump-announce feedback and reveal scrolling, retire the album digit count prefix, add shared bump/reveal helpers, unit tests, a real-key e2e probe, and key docs.

## Notes

[2026-11-17T20:43:53Z · bob-cli-mu.1] -r check prior work notes

[2026-11-17T21:01:48Z · bob-cli-mu.1] PROPOSED FOLLOW-UP: docs-check lint flags docs/reference/json-outputs.md at 6089 words (cap 6000) — that file lives in the bob-cli checkout assembled by the checker, untouched by this phase; consider a budget bump or trim

[2026-11-17T21:01:57Z · bob-cli-mu.1] PROPOSED FOLLOW-UP: five timing-budget unit tests (event-link-times, frees-marks, keep-moving-marks-surface, off-clock-link-chips, dependencies-stage-entry-and-view) fail under full-suite load but pass in isolation on both trees; consider raising budgets or quarantining them as perf

[2026-11-17T21:02:11Z · bob-cli-mu.1] field-nav done in bob-plugins: painted-order helpers shared by targets and body painter (issues now before + field), Shift+J/K steps and 1-9 jumps with clamp-bump-announce and group reveal, count prefix retired, shared bump/reveal helpers, announcer unhidden, 16-test suite green, affected suites green (92 pass/1 skip), build+build:check+docs inventory green, e2e CDP probe added (wrappers green; no Obsidian here so real walk not run). Ship blocked: vault sync refused by live workspace-15 deploy (agent eo RUNNING) — land agent should sync after it lands; docs lint json-outputs budget and load-flaky perf budgets recorded as follow-ups.

## Dependencies

- **Blocks:** [bob-cli-mu.2](bob-cli-mu.2.md) ✓ · ⧖ 2026-11-17
- **Blocks:** [bob-cli-mu.3](bob-cli-mu.3.md) ✓ · ⧖ 2026-11-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-mu.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-mu.1/README.md) | [bob-cli-mu.1](bob-cli-mu.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@137c77f`](https://github.com/bobs-org/bob-plugins/commit/137c77f60dbf39494b1b47e519ad61c930bfa9e2) | feat(schema-card): jump between fields with Shift+J/K and 1-9 in painted order | [bob-cli-mu.1](bob-cli-mu.1.md) | 2026-11-17 16:04:12 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-mu.1][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-mu.1/README.md

<!-- sase:referenced-by:end -->
