# Bead: bob-cli-hn.6.1.3 — Apply guarded verdicts and recover dependents with Undo snapshots

[Bead Pages](../README.md) / [bob-cli-hn.6.1](bob-cli-hn.6.1.md) / bob-cli-hn.6.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-hn.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hn.6.md) · **Assignee:** `bob-cli-hn.6.1.3` · **Size:** medium
**Created:** 2026-11-05 20:37:46 EST · **Closed:** 2026-11-05 22:47:48 EST
**Plan:** [202611/cycler\_offer\_verdicts.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/cycler_offer_verdicts.md)

## Description

verdict_apply: implement the internal Now verdict transaction, per-row stale refusal, root-only Done and Cancel, joint recover-only cascades, truthful receipts, and exact guarded Undo snapshots; leave gesture wiring dormant.

## Notes

[2026-11-06T03:47:15Z · bob-cli-hn.6.1.3] PROPOSED FOLLOW-UP: clean-base docs-check lychee fails in task-merge (file:///capture#merging-tasks-into-a-new-task-with) on plugin HEAD ef9257d; identical with and without verdict_apply changes

[2026-11-06T03:47:21Z · bob-cli-hn.6.1.3] PROPOSED FOLLOW-UP: clean-base test-task-link-marks-motion fails (production CSS reduced-motion, 1 fail, ~90s) on plugin HEAD ef9257d; identical with and without verdict_apply changes

[2026-11-06T03:47:48Z · bob-cli-hn.6.1.3] verdict_apply done: added 089i applyOfferClosesNow with guarded root+recovery writes, joint attribution, receipt/Undo; tests test-task-status-cycler-successor-apply (6 pass) + verdicts (7 pass); build pass; full npm test 5624/5625 (1 clean-base motion fail recorded); docs-check clean-base lychee fail recorded; bob plugins sync --repo linked done

## Dependencies

- **Depends on:** [bob-cli-hn.6.1.2](bob-cli-hn.6.1.2.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hn.6.1.4](bob-cli-hn.6.1.4.md) ✓ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-hn.6.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hn.6.1.3/README.md) | [bob-cli-hn.6.1.3](bob-cli-hn.6.1.3.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:195--code][1] | Recheck closed child scope | 2 |
| read-by | [agent:bob-cli-hn.6.1.3][2] | verify notes recorded | 2 |
| read-by | [agent:bob-cli-hn.6.1.land--1][3] | Recheck current landing scope, close notes, and prior follow-up tracker status | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.195.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hn.6.1.3/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hn.6.1.land.md

<!-- sase:referenced-by:end -->
