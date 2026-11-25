# Bead: bob-cli-ph.7.1.1 — Bold plugin writers and verbatim project conversion

[Bead Pages](../README.md) / [bob-cli-ph.7.1](bob-cli-ph.7.1.md) / bob-cli-ph.7.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ph.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.7.md) · **Assignee:** `bob-cli-ph.7.1.1` · **Size:** medium
**Created:** 2026-11-25 08:48:55 EST · **Closed:** 2026-11-25 09:37:05 EST
**Plan:** [202611/obsidian\_true\_case\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/obsidian_true_case_drawers.md)

## Description

bold-writers-and-conversion: switch new plugin drawer writes to bold, refresh Rust-owned fixtures, and preserve valid titles and empty sections through promotion and reversal.

## Notes

[2026-11-25T14:36:53Z · bob-cli-ph.7.1.1] Changed plugins: task-status-cycler, bob-navigation-hotkeys (src fragments + built main.js + fixtures + 3 test files). New writes emit bold drawer headers via centralized taskBlockDrawerHeaderBody/Line; TASK_BLOCK_NOTES_TITLE is now Notes with NOTES key unchanged; reversal bullets are `- **Title**` verbatim with named (not_a_drawer_title/reserved) refusals; empty eligible H2 sections and explicit empty bold drawers round-trip; Notes role fixed for bold markers. Deployed via documented non-forcing recipe (ff to a971285, no -F). Markers: bob-task-drawer-bold-writes-v1 in both bundles. Full docs consolidation left to obsidian-acceptance per plan.

[2026-11-25T14:37:05Z · bob-cli-ph.7.1.1] Verified: 201 focused tests pass (drawer/req twin copies, task-split vectors+carry+gesture, project-from-task, project-reversal, creation bytes, promotion suites), npm run validate 12/12, build --check clean. Canonical fixtures refreshed (task_reqs layout/writes, task_split vectors). Legacy headers reused verbatim, never respelled. Both plugins synced to vault from a971285-based uncommitted build.

## Dependencies

- **Blocks:** [bob-cli-ph.7.1.2](bob-cli-ph.7.1.2.md) ◐ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-ph.7.1.4](bob-cli-ph.7.1.4.md) ◐ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ph.7.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.7.1.1/README.md) | [bob-cli-ph.7.1.1](bob-cli-ph.7.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@f2e8c62`](https://github.com/bobs-org/bob-plugins/commit/f2e8c62a29464701cb097233579c156964cb4996) | feat(task-drawers)!: emit bold drawer headers and verbatim project conversion in plugins | [bob-cli-ph.7.1.1](bob-cli-ph.7.1.1.md) | 2026-11-25 09:38:13 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ph.7.1.1][1] | check notes and remaining work | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.7.1.1/README.md

<!-- sase:referenced-by:end -->
