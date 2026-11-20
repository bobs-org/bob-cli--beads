# Bead: bob-cli-nj.3 — bob-plugins: Task Card picker log stages

[Bead Pages](../README.md) / [bob-cli-nj](README.md) / bob-cli-nj.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.f3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.f3.md) · **Assignee:** `bob-cli-nj.3` · **Size:** medium
**Created:** 2026-11-19 12:14:03 EST · **Closed:** 2026-11-19 15:59:50 EST
**Plan:** [202611/log\_reason\_recall.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/log_reason_recall.md)

## Description

picker-stages: attach recall to the schedule-review form (a Schedule reason field and a Work summary field sharing one band that follows focus) and to the schedule-work-log, lane-release-reason, and cancel-reason stages. Ctrl+N/P route through the picker keydown mixin, Esc and Ctrl+[ back out in layers, and the writers call noteUsed.

## Notes

[2026-11-19T20:59:39Z · bob-cli-nj.3] PROPOSED FOLLOW-UP: docs-check budget over in mac-capture docs (capture-previews 6171, keyboard 6027 vs 6000 cap) reproduces without this phase — trim or raise cap

[2026-11-19T20:59:50Z · bob-cli-nj.3] picker-stages done: schedule-review shared band with Tab kind swap and pinned max height, schedule-work-log/lane-release/cancel recall via keydown mixin with Esc/Ctrl+[ layering, noteUsed on schedule/work/cancel writes; 123 tests pass, build clean, docs-check shows only pre-existing mac-capture budget errors, sync refused by running ws16 deploy for land to retry after commit

## Dependencies

- **Depends on:** [bob-cli-nj.2](bob-cli-nj.2.md) ✓ · ⧖ 2026-11-19
- **Blocks:** [bob-cli-nj.8](bob-cli-nj.8.md) ✓ · ⧖ 2026-11-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-nj.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nj.3/README.md) | [bob-cli-nj.3](bob-cli-nj.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@3968f0d`](https://github.com/bobs-org/bob-plugins/commit/3968f0d70e8d45a1c225a6bb111df3f1805a956e) | feat(log-recall): attach recall to Task Card picker log stages | [bob-cli-nj.3](bob-cli-nj.3.md) | 2026-11-19 16:01:14 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-nj.3][1] | Need full bead with notes | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nj.3/README.md

<!-- sase:referenced-by:end -->
