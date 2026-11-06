# Bead: bob-cli-ho.5 — Stage-end ticks and staged-advance regression tests in navigation

[Bead Pages](../README.md) / [bob-cli-ho](README.md) / bob-cli-ho.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.193](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.193.md) · **Assignee:** `bob-cli-ho.5` · **Size:** small
**Created:** 2026-11-05 18:44:51 EST · **Closed:** 2026-11-05 20:50:41 EST
**Plan:** [202611/gtd\_checklist\_stages.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gtd_checklist_stages.md)

## Description

nav_ticks: add the quiet STAGE ✓ tick to Ctrl+Enter done lines when a stage's last due row is completed, and lock in queue-order advance when the next staged row sits above the cursor.

## Notes

[2026-11-06T01:50:41Z · bob-cli-ho.5] Implemented stage-end ticks in Ctrl+Enter notices and added regressions for final-stage completion, unfinished stages, and queue-order advance to a row above the cursor. Verified navigation tests (17/17), plugin build check, clean diff check, and deployed the plugin with bob plugins sync.

## Dependencies

- **Depends on:** [bob-cli-ho.3](bob-cli-ho.3.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-ho.6](bob-cli-ho.6.md) ◐ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ho.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ho.5/README.md) | [bob-cli-ho.5](bob-cli-ho.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@2d0348b`](https://github.com/bobs-org/bob-plugins/commit/2d0348b2d9e3b639142387417c4b7d1007afa48c) | feat(navigation): mark completed checklist stages | [bob-cli-ho.5](bob-cli-ho.5.md) | 2026-11-05 20:51:18 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ho.5][1] | Check prior phase notes before implementation | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ho.5/README.md

<!-- sase:referenced-by:end -->
