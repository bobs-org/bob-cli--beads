# Bead: bob-cli-bk.2 — Apply inbox route answers inside the capture batch

[Bead Pages](../README.md) / [bob-cli-bk](README.md) / bob-cli-bk.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.a9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.a9.md) · **Assignee:** `bob-cli-bk.2` · **Size:** medium
**Created:** 2026-10-24 14:00:27 EDT · **Closed:** 2026-10-24 16:32:14 EDT
**Plan:** [202610/capture\_inbox\_routing.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_inbox_routing.md)

## Description

route-apply: `-i/--inbox-route` answers move candidates through the task-move engine inside the same capture batch, with freshness stamps, link repair, refusals, followed mirrors, and docs.

## Notes

[2026-10-24T20:12:23Z · bob-cli-bk.2] PROPOSED FOLLOW-UP: skipped decisions:reference record for capture inbox routing (memory_decision_record=no) — add decisions:capture-asks-where-inbox-tasks-go in a later phase

[2026-10-24T20:12:30Z · bob-cli-bk.2] PROPOSED FOLLOW-UP: docs-check published-URLs fails on stale live URL reference/cli/relations/ (no such page in this tree; unrelated to bk.2 page set)

[2026-10-24T20:26:35Z · bob-cli-bk.2] PROPOSED FOLLOW-UP: completion kinds decisions missing for themes rename:old/new (pre-existing on clean base; every_value_arg test still red after bk.2 adds capture:inbox-route)

[2026-10-24T20:26:41Z · bob-cli-bk.2] PROPOSED FOLLOW-UP: 4 completion/help CLI tests red on clean base (bash wordbreak, 2x capture_text named_start, capture_complete help alphabetical) — unrelated to bk.2

[2026-10-24T20:32:14Z · bob-cli-bk.2] route-apply landed: -i/--inbox-route answers move candidates through task-move in-batch (act-then-move, freshness stamp, link repair, closed+line selectors); stale/refused refusals with payloads; trackers/open_notes follow; human routed/kept rows. Verified: 15 CLI vector tests (IRA1-IRA15 incl. dry==real, 2-dest bulk, rollback unit test), task_move unit tests, fmt+clippy gates, docs-gen+docs-check strict build. Remaining reds (completion kinds themes args, 4 completion/help tests, relations published URL) reproduce on clean base with PROPOSED FOLLOW-UP notes.

## Dependencies

- **Depends on:** [bob-cli-bk.1](bob-cli-bk.1.md) ✓ · ⧖ 2026-10-24
- **Blocks:** [bob-cli-bk.3](bob-cli-bk.3.md) ✓ · ⧖ 2026-10-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-bk.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bk.2/README.md) | [bob-cli-bk.2](bob-cli-bk.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4f13e97`](https://github.com/bobs-org/bob-cli/commit/4f13e979eb3dba1a69c840bfb2c34a9d0ff7ecd6) | feat(capture): route inbox answers through task-move engine | [bob-cli-bk.2](bob-cli-bk.2.md) | 2026-10-24 16:34:24 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-bk.2][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bk.2/README.md

<!-- sase:referenced-by:end -->
