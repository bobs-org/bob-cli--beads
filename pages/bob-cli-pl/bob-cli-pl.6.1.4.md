# Bead: bob-cli-pl.6.1.4 — Route area and project settings entry points and project task handoffs

[Bead Pages](../README.md) / [bob-cli-pl.6.1](bob-cli-pl.6.1.md) / bob-cli-pl.6.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pl.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pl.6.md) · **Assignee:** `bob-cli-pl.6.1.4` · **Size:** medium
**Created:** 2026-11-24 15:49:21 EST · **Closed:** 2026-11-25 06:39:40 EST
**Plan:** [202611/area\_project\_settings.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/area_project_settings.md)

## Description

settings-entrypoints: register area/project in the existing registry, route card actions by setting id, implement project-task navigation and handoffs, and document the API and bare-plus keys.

## Notes

[2026-11-25T11:39:12Z · bob-cli-pl.6.1.4] PROPOSED FOLLOW-UP: docs-check lint budgets over in untouched reference docs — bob-docs lint reports 3 over-budget errors (reference/mac-capture/keyboard.md, reference/mac-capture/protocol.md, reference/plugins/bob-navigation-hotkeys.md); reproduced identically on the clean base tree via git stash, so pre-existing and out of scope for this phase

[2026-11-25T11:39:26Z · bob-cli-pl.6.1.4] PROPOSED FOLLOW-UP: two load-sensitive perf budget flakes under full-suite contention — test-ledger-tools-event-link-times and test-ledger-tools-frees-marks 25ms budgets failed once during full npm test (9422/9429 pass) and pass in isolation on this tree; neither area was touched by this phase

[2026-11-25T11:39:40Z · bob-cli-pl.6.1.4] settings-entrypoints landed and verified: area/project registered in the == registry (bank precedence, teardown intact); setting/focusSettings requests route ==, Settings, and policy chips onto settings rows incl. ghosts with alias mapping and degraded fallback; project Goal/Starts/Depends-on/status hand off to the Task Card with line validation, cursor fallback, and no writes; docs updated (property-editor, area-and-project-cards, architecture seam). Evidence: new settings-entrypoints suite 19/19, neighbors 97/97 + 118/119 (1 pre-existing skip), full npm test 9422/9429 with only 2 load-flake perf budgets that pass in isolation; build:check, inventory:check, and bob plugins sync clean; docs-check lint failures proven pre-existing on clean base.

## Dependencies

- **Depends on:** [bob-cli-pl.6.1.3](bob-cli-pl.6.1.3.md) ✓ · ⧖ 2026-11-24
- **Blocks:** [bob-cli-pl.6.1.5](bob-cli-pl.6.1.5.md) ✓ · ⧖ 2026-11-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pl.6.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pl.6.1.4/README.md) | [bob-cli-pl.6.1.4](bob-cli-pl.6.1.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@876782f`](https://github.com/bobs-org/bob-plugins/commit/876782fed9878db3a1f3db5f0c33bb8ed4d6ab7d) | feat(props): route area/project settings entry points and project task handoffs | [bob-cli-pl.6.1.4](bob-cli-pl.6.1.4.md) | 2026-11-25 06:41:06 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pl.6.1.4][1] | Need the phase scope and design file | 3 |
| read-by | [agent:bob-cli-pl.6.1.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pl.6.1.4/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pl.6.1.land/README.md

<!-- sase:referenced-by:end -->
