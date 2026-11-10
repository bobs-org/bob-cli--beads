# Bead: bob-cli-js.2 — Configured task-type minutes in Stats

[Bead Pages](../README.md) / [bob-cli-js](README.md) / bob-cli-js.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.41.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.41.linker.w0.md) · **Assignee:** `bob-cli-js.2` · **Size:** medium
**Created:** 2026-11-10 11:49:24 EST · **Closed:** 2026-11-10 12:37:54 EST
**Plan:** [202611/period\_strip\_two\_charts.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/period_strip_two_charts.md)

## Description

type_split: add a task_type parts dimension to Pomodoro metrics that splits each session's counted minutes over its configured types only, with unnamed and label-only buckets, plus docs.

## Notes

[2026-11-10T17:37:40Z · bob-cli-js.2] PROPOSED FOLLOW-UP: just docs-check fails on clean base with bob-plugins mount collision (reference/plugins index.md); same error with and without type_split changes

[2026-11-10T17:37:54Z · bob-cli-js.2] type_split done: task_type parts with off-clock mirror, buckets @unnamed/@other_names, theme_hues extended, docs updated; verified 7 new task_type tests pass, 229 stats + 47 periods tests green, cargo fmt clean

## Dependencies

- **Blocks:** [bob-cli-js.3](bob-cli-js.3.md) ◐ · ⧖ 2026-11-10

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-js.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-js.2/README.md) | [bob-cli-js.2](bob-cli-js.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`beef7f2`](https://github.com/bobs-org/bob-cli/commit/beef7f27bf4668693245b80855680bfad886b5d6) | feat(stats): add task\_type parts dimension with configured-type split | [bob-cli-js.2](bob-cli-js.2.md) | 2026-11-10 12:39:27 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-js.2][1] | Verify scope before closing | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-js.2/README.md

<!-- sase:referenced-by:end -->
