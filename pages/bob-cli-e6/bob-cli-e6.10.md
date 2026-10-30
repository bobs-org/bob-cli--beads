# Bead: bob-cli-e6.10 — Ctrl+Shift+M Pomodoro bullet moves retype tasks

[Bead Pages](../README.md) / [bob-cli-e6](README.md) / bob-cli-e6.10

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2t.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2t.linker.w0.md) · **Assignee:** `bob-cli-e6.10` · **Size:** medium
**Created:** 2026-10-29 16:16:34 EDT · **Closed:** 2026-10-29 22:43:04 EDT
**Plan:** [202610/task\_types.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_types.md)

## Description

move-retype: make the Pomodoro bullet move picker apply the retype rule with Enter, Alt+Enter keep-type merges, and Tab component cycling, with consequence footers and checked cross-note writes.

## Notes

[2026-10-30T02:37:37Z · bob-cli-e6.10] PROPOSED FOLLOW-UP: Five task-card theme tests still fail identically on clean base d3a8ff4 (theme notices, no-op batches, save notices, stage-row subtitle, theme-menu-grey); corroborates the existing follow-up recorded on bob-cli-e8.8. Full npm test otherwise reaches the suite; these failures are unrelated to this phase.

[2026-10-30T02:43:04Z · bob-cli-e6.10] Implemented Pomodoro bullet move retyping, composite type cycling, Alt+Enter type merge, dynamic D10 consequences, and guarded same-note/cross-note writes in bob-navigation-hotkeys; updated docs and added picker/write tests. Focused picker and move suites pass (70/70); build and docs:check pass; bob-navigation-hotkeys synced. Full npm test has five task-card theme failures reproduced identically on clean base d3a8ff4 and recorded as a proposed follow-up citing bob-cli-e8.8. epic-symbols was empty.

## Dependencies

- **Blocks:** [bob-cli-e6.13](bob-cli-e6.13.md) ◐ · ⧖ 2026-10-29
- **Depends on:** [bob-cli-e6.8](bob-cli-e6.8.md) ✓ · ⧖ 2026-10-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-e6.10](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-e6.10/README.md) | [bob-cli-e6.10](bob-cli-e6.10.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@a42de4d`](https://github.com/bobs-org/bob-plugins/commit/a42de4d4fc49891d43700bcefad6f2c6479ec522) | feat(navigation): retype moved Pomodoro tasks | [bob-cli-e6.10](bob-cli-e6.10.md) | 2026-10-29 22:44:02 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-e6.10][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-e6.11][2] | Need move-retype landing as the sibling picker pattern | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-e6.10/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-e6.11/README.md

<!-- sase:referenced-by:end -->
