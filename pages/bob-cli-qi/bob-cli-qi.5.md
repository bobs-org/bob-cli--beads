# Bead: bob-cli-qi.5 — Re-run the retired project-count cleanup in the vault

[Bead Pages](../README.md) / [bob-cli-qi](README.md) / bob-cli-qi.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1gn](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1gn.md) · **Assignee:** `bob-cli-qi.5` · **Size:** small
**Created:** 2026-11-26 10:06:12 EST · **Closed:** 2026-11-26 11:38:15 EST
**Plan:** [202611/bank\_hub\_demotion.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_hub_demotion.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:17c634843198ceb669c31f8c | attached via sase artifact create --bead |
| related | file:explicit:3fdb456209a6a6243b07c8e5 | attached via sase artifact create --bead |
| related | file:explicit:59a92613628abb20d848ee54 | attached via sase artifact create --bead |
| related | file:explicit:5a1b0a3002c2d3d991e08131 | attached via sase artifact create --bead |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

count-sweep: dry-run the landed retire-project-count-keys tool against the live vault with a current bob. If any host recreated task_count/open_task_count, attribute that host and apply the guarded cleanup, then prove a repeat dry-run is a no-op and retain the receipts.

## Notes

[2026-11-26T16:38:02Z · bob-cli-qi.5] PROPOSED FOLLOW-UP: prior count-sweep receipt file:explicit:7e981553181fd23c81d6b221 resolves as missing; superseded by new receipts file:explicit:3fdb456209a6a6243b07c8e5 (summary), file:explicit:59a92613628abb20d848ee54 (apply), file:explicit:5a1b0a3002c2d3d991e08131 (pre dry-run), file:explicit:17c634843198ceb669c31f8c (post no-op proof)

[2026-11-26T16:38:15Z · bob-cli-qi.5] count-sweep done: dry-run found 106 notes/212 retired keys, attributed to kellys-macbook-pro-local stale pre-retirement bob-project-tasks writer (Nov-24 re-adds after apollo cleanup 79754d7f9); Mac now current (plugin 1.2.0, bob 0.6.0, Obsidian relaunched). Guarded apply removed all 212 keys with 0 skipped; repeat dry-run at vault snapshot b927855b is a no-op (0/0/0); vault-sync healthy, local==remote. Receipts: file:explicit:3fdb456209a6a6243b07c8e5, file:explicit:59a92613628abb20d848ee54, file:explicit:5a1b0a3002c2d3d991e08131, file:explicit:17c634843198ceb669c31f8c.

## Dependencies

- **Depends on:** [bob-cli-qi.1](bob-cli-qi.1.md) ✓ · ⧖ 2026-11-26
- **Depends on:** [bob-cli-qi.2](bob-cli-qi.2.md) ✓ · ⧖ 2026-11-26
- **Depends on:** [bob-cli-qi.3](bob-cli-qi.3.md) ✓ · ⧖ 2026-11-26
- **Blocks:** [bob-cli-qi.6](bob-cli-qi.6.md) ✓ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-qi.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-qi.5/README.md) | [bob-cli-qi.5](bob-cli-qi.5.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:research.6k.gem][1] | Inspect in-progress phase details and progress notes of qi and qj epics | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.6k.gem/README.md

<!-- sase:referenced-by:end -->
