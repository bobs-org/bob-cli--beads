# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.2 — Restore the Task Card cleanup in BulletPropertyPickerModal.onClose

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.2` · **Size:** small
**Created:** 2026-10-25 11:34:35 EDT · **Closed:** 2026-10-25 11:41:19 EDT
**Plan:** [202610/backlog\_batch11\_ref\_repair\_taskcard\_popout\_gkeep\_again.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch11_ref_repair_taskcard_popout_gkeep_again.md)

## Description

task-card-close-cleanup: resolve bob-cli-4e by folding the dead Task Card class removal and flag resets into the live onClose in bob-navigation-hotkeys src/350-picker-task-card.js, with a focused test and a bob plugins sync deploy.

## Notes

[2026-10-25T15:41:19Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.2] Restored Task Card close cleanup in 350-picker-task-card.js onClose (removes bob-task-card-modal/wide, resets linkResolving and taskCardDispatching before super.onClose, no reorder of route-cancel/review-settle). Added focused test in test-navigation-hotkeys-picker-lifecycle.cjs (open Task Card, close, assert classes+flags cleared) — failed before fix, passes after build. Ran npm run build, npm test (3666 pass), npm run validate (7/7 valid). Deployed via bob plugins sync --repo to vault; bob-navigation-hotkeys 2.56.4, vault main.js now matches. Left bob-cli-4e open for lander.

## Dependencies

- **Blocks:** [bob-cli-an.6.6.6.5.6.5.5.6.6.6.3](bob-cli-an.6.6.6.5.6.5.5.6.6.6.3.md) ✓ · ⧖ 2026-10-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.2/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.2](bob-cli-an.6.6.6.5.6.5.5.6.6.6.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@c07b125`](https://github.com/bobs-org/bob-plugins/commit/c07b1257178e76034ee668e4a4d040e1cbb5d0ed) | fix(nav-hotkeys): restore Task Card close cleanup in onClose | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.2](bob-cli-an.6.6.6.5.6.5.5.6.6.6.2.md) | 2026-10-25 11:42:01 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.2][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.2/README.md

<!-- sase:referenced-by:end -->
