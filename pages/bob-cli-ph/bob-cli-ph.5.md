# Bead: bob-cli-ph.5 — Drawer rename respells and inventories legacy drawers

[Bead Pages](../README.md) / [bob-cli-ph](README.md) / bob-cli-ph.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5x.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5x.linker.w0.md) · **Assignee:** `bob-cli-ph.5` · **Size:** medium
**Created:** 2026-11-22 17:36:48 EST · **Closed:** 2026-11-25 09:52:42 EST
**Plan:** [202611/true\_case\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/true_case_drawers.md)

## Description

drawer-rename: `bob task rename-drawer` writes NEW verbatim, allows case-only respelling, and gains a read-only legacy inventory for the migration.

## Notes

[2026-11-25T14:26:18Z · bob-cli-ph.5] PROPOSED FOLLOW-UP: docs-check plugin page budgets — docs/reference/plugins/bob-navigation-hotkeys.md is 46 words over its 6000-word cap and docs/develop/plugins/plugin-apis.md warns at 9287/8000; both reproduce identically on clean HEAD.

[2026-11-25T14:52:42Z · bob-cli-ph.5--1] Verified landed rename/inventory implementation; focused unit and CLI tests, docs generation, and monitored just check passed. Clean-base docs-check overages are recorded as a proposed follow-up; no epic symbols remain.

## Dependencies

- **Depends on:** [bob-cli-ph.4](bob-cli-ph.4.md) ✓ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-ph.9](bob-cli-ph.9.md) ✓ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ph.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.5.md) | [bob-cli-ph.5](bob-cli-ph.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ae42b3e`](https://github.com/bobs-org/bob-cli/commit/ae42b3ed2a48ddc218021262c0fdd3fc791d99a1) | feat(task-drawers): preserve rename spelling and inventory legacy drawers | [bob-cli-ph.5](bob-cli-ph.5.md) | 2026-11-25 09:29:31 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ph.6.1.2][1] | Check existing tracking for the same docs budget failure | 1 |
| read-by | [agent:bob-cli-ph.land][2] | Need the child scope and notes | 1 |
| read-by | [agent:g1][3] | Check whether phase is blocked on the release gate | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.6.1.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.land.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.g1/README.md

<!-- sase:referenced-by:end -->
