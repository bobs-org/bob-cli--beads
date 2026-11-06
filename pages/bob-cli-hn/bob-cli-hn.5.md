# Bead: bob-cli-hn.5 — Nav cancel API v1 and Unblocked notice v4

[Bead Pages](../README.md) / [bob-cli-hn](README.md) / bob-cli-hn.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.191](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.191/README.md) · **Assignee:** `bob-cli-hn.5` · **Size:** small
**Created:** 2026-11-05 18:41:47 EST · **Closed:** 2026-11-05 19:46:28 EST
**Plan:** [202611/successor\_card\_verdicts.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/successor_card_verdicts.md)

## Description

nav-apis: expose a pure Task-Card-parity cancel planner as api.cancel v1, and extend api.notice to v4 with offer-close rows, refusal lines, tickler lines, and a guarded Undo action.

## Notes

[2026-11-06T00:46:21Z · bob-cli-hn.5] PROPOSED FOLLOW-UP: Stabilize unrelated bob-plugins gates — npm test reports configured theme menu vector mismatches (expected SNACK, got NACK) in two suites and a pre-existing Pomodoro theme fixture byte-copy mismatch; npm run docs:check reports generated drift in docs/reference/glossary.md. The reduced-motion browser failure from the first full run passed when isolated; related prior tracking: bob-cli-f5.

[2026-11-06T00:46:28Z · bob-cli-hn.5] Implemented nav api.cancel v1 with the fixed Task Card blank-reason fallback, api.notice v4 offer-close/refusal/tickler/guarded-Undo rendering, docs, and tests. Targeted API and notice tests pass; plugin build passes and bob plugins sync completed. Full npm test retains three unrelated fixture failures; docs:check retains generated glossary drift, recorded as a proposed follow-up.

## Dependencies

- **Depends on:** [bob-cli-hn.4](bob-cli-hn.4.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hn.6](bob-cli-hn.6.md) ◐ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-hn.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hn.5/README.md) | [bob-cli-hn.5](bob-cli-hn.5.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hn.5][1] | Need the phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hn.5/README.md

<!-- sase:referenced-by:end -->
