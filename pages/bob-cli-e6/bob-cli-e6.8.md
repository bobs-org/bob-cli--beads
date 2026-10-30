# Bead: bob-cli-e6.8 — Ledger Tools type model and routing mirror

[Bead Pages](../README.md) / [bob-cli-e6](README.md) / bob-cli-e6.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2t.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2t.linker.w0.md) · **Assignee:** `bob-cli-e6.8` · **Size:** medium
**Created:** 2026-10-29 16:16:34 EDT · **Closed:** 2026-10-29 21:49:34 EDT
**Plan:** [202610/task\_types.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_types.md)

## Description

js-mirror: mirror storage, config, the cascade, and the four routing planners in Ledger Tools JS against the copied vectors, extend api.themes additively, and update every plugin-local name helper.

## Notes

[2026-10-30T01:48:55Z · bob-cli-e6.8] PROPOSED FOLLOW-UP: 4 pre-existing test-navigation-task-card-theme-edit.cjs failures (helpers.taskCardThemeUnchangedNotice/taskCardThemeSavedNotice/taskCardThemeStageItem are not functions) plus 1 is-muted pill failure in test-navigation-task-card-view.cjs reproduce identically on the clean base tree; 2 perf tests flake only under full-suite load and pass solo on both trees

[2026-10-30T01:49:34Z · bob-cli-e6.8] js-mirror done in bob-plugins: vectors copied byte-for-byte (pin 17504745) with agree/retype/place/relocate runners green (38/38); model reads type+theme keys and emits [type::]; suggest adds task_type-first defaults, type_default_conflict, and the default step; caps parse default_type/reading_type with both-present invalid; new 279-plugin-task-type-routing.js exported; api.themes gains 6 additive methods with planThemeChange kept legacy except linkOnce merge; plugin-apis.md documented; 165/076 pickers prefer typeComponentsOf; 315/085c verified key-agnostic; downstream [type::] byte assertions updated. Full npm test 4321/4328: 8 fixed-by-contract, remaining 5 pre-existing (4 TypeError + is-muted, identical on clean tree) + 2 load flakes green solo; recorded as PROPOSED FOLLOW-UP. Deployed via bob plugins sync (3 plugins). No epic symbols left.

## Dependencies

- **Blocks:** [bob-cli-e6.10](bob-cli-e6.10.md) ✓ · ⧖ 2026-10-29
- **Blocks:** [bob-cli-e6.11](bob-cli-e6.11.md) ✓ · ⧖ 2026-10-29
- **Blocks:** [bob-cli-e6.12](bob-cli-e6.12.md) ○ · ⧖ 2026-10-29
- **Depends on:** [bob-cli-e6.5](bob-cli-e6.5.md) ✓ · ⧖ 2026-10-29
- **Blocks:** [bob-cli-e6.9](bob-cli-e6.9.md) ✓ · ⧖ 2026-10-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-e6.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-e6.8/README.md) | [bob-cli-e6.8](bob-cli-e6.8.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@d3a8ff4`](https://github.com/bobs-org/bob-plugins/commit/d3a8ff40b1b2aebce3adb1addd5a8cadae59df70) | feat(ledger-tools): mirror task types, default type, and routing planners | [bob-cli-e6.8](bob-cli-e6.8.md) | 2026-10-29 21:51:34 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-e6.11][1] | Need js-mirror landing so link-picker-retype can reuse the routing API | 1 |
| read-by | [agent:bob-cli-e6.8][2] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-e6.11/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-e6.8/README.md

<!-- sase:referenced-by:end -->
