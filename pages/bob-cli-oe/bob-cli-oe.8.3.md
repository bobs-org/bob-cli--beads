# Bead: bob-cli-oe.8.3 — Land the jump after every write in task-status-cycler and block-id-prompt

[Bead Pages](../README.md) / [bob-cli-oe.8](bob-cli-oe.8.md) / bob-cli-oe.8.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-oe.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-oe.land.md) · **Assignee:** `bob-cli-oe.8.3` · **Size:** medium
**Created:** 2026-11-20 21:39:29 EST · **Closed:** 2026-11-21 08:24:57 EST
**Plan:** [202611/successor\_jump\_repairs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/successor_jump_repairs.md)

## Description

cycler-jump-ordering: make the Task Link Ctrl+Enter close and the unlink-plus-inbox-route path land the jump only after their strike or move writes and walk settle, stop the walk-return receipt doubling the ↗ line, and build the Left identity from the fresh plan row.

## Notes

[2026-11-21T13:24:57Z · bob-cli-oe.8.3] Cycler jump ordering landed: Task Link Ctrl+Enter finalizes in return mode then strikes then lands (walk return stays via follow); unlink+inbox-route returns the parked jump, moves, then settles with follow or lands after notice (older cyclers keep today's order); work-summary modal closes before landing; walk-return cards omit the jump receipt; Left identity builds from the fresh plan row with fallback, covering refused picks and cancelled closes. Verified: 134 cycler focused tests pass, 65 block-id focused pass, 233 nav suites pass, full unit 8032 pass with only 2 known ledger 25ms flakes, docs-check shows only known vault-format budget failure, build:check clean, manifests bumped to 1.52.1/1.39.1 and bob plugins sync deployed as descendant of 1a95b29.

## Dependencies

- **Depends on:** [bob-cli-oe.8.2](bob-cli-oe.8.2.md) ✓ · ⧖ 2026-11-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-oe.8.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-oe.8.3/README.md) | [bob-cli-oe.8.3](bob-cli-oe.8.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@6debb63`](https://github.com/bobs-org/bob-plugins/commit/6debb63b4c12caa600e58eb71b5044bb9b40a84a) | feat(task-status-cycler): implement cycler jump ordering | [bob-cli-oe.8.3](bob-cli-oe.8.3.md) | 2026-11-21 08:26:02 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-oe.8.3][1] | Need final status before close | 3 |
| read-by | [agent:bob-cli-oj.2][2] | Need whether the cycler v6 park-the-walk test failure is already tracked on the jump-pin landing phase | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-oe.8.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-oj.2/README.md

<!-- sase:referenced-by:end -->
