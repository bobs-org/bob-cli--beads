# Bead: bob-cli-gm.1 — Target-run grammar in both resolvers, fan-out, and grammar bump

[Bead Pages](../README.md) / [bob-cli-gm](README.md) / bob-cli-gm.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.17k](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.17k.md) · **Assignee:** `bob-cli-gm.1` · **Size:** large
**Created:** 2026-11-03 13:55:33 EST · **Closed:** 2026-11-03 21:10:44 EST
**Plan:** [202611/capture\_multi\_target.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_multi_target.md)

## Description

grammar: recognize a leading or trailing run of `@route+id` markers in the execution resolver and the capture-parse resolver, fan each run out into one parsed item per target, report `targets[]` and the new refusals in capture-parse, bump the grammar revision, and document the grammar contract.

## Notes

[2026-11-03T19:01:11Z · bob-cli-gm.1] PROPOSED FOLLOW-UP: Reconcile the incomplete-target example in the epic contract — the design says @work+a @dev+ note needs block_id, but editor_classify.rs sets Need::Task for a missing + ID and grammar.rs plus tests/cli/capture/parse.rs assert task for singleton @dev+. The same design requires existing per-member needs and unchanged singleton output. The phase plan will preserve the existing classifier and union its needs; the epic land agent should reconcile that example with the equivalence rule.

[2026-11-03T21:47:46Z · bob-cli-gm.1] REMAINING WORK: At clean base 0b4cebdf, both resolvers still select one marker; no FanoutContext, targets wire field, or new refusal codes have landed. Reviewed the earlier capture_target_run_grammar tale and prepared a validated four-phase child epic: shared selection/member views, execution fan-out, editor targets, then joint activation/revision/docs and full verification. Public behavior stays unchanged until both adapters are ready. Code reports grammar 7 while docs claim 8, so activation must rescan and currently take 9. No production files changed or code tests run in this planning turn; epic-symbols reports no entries. The child epic land agent must complete and close this phase after its children, leaving bob-cli-gm to its own land agent.

[2026-11-04T00:06:50Z · bob-cli-gm.1.1.4] Activation phase bob-cli-gm.1.1.4 re-scanned the active code and docs claims and activated both target-run parsers at capture-language revision 9. Keep revision 9 as the open fan-out phases integrate; do not lower it.

[2026-11-04T02:11:25Z · bob-cli-gm.1.1.land] Closeout evidence for delegated target-run grammar phase. The approved child epic bob-cli-gm.1.1 completed; SASE normal close of that child also closed this phase with reason delegated work landed. Grammar revision 9 is active in both parsers: selected-run duplicate checks, split-edge refusal precedence, per-target execution/template fan-out with terminal schedule/priority semantics, single editor item with targets and exact spans, coded refusals, and preserved singleton Need::Task behavior. Verification: named sase tool run check 75c13c781669fb3c04788943911c8868 succeeded; focused target-run, capture-parse/dry-run scratch-vault, catalog protocol/count 70, help snapshots, docs-reference generator, and git diff --check passed. just docs-check lint passed; generated drift still stops at unchanged sase/memory/glossary/task-merge.md (missing front matter), already routed to bob-cli-go, with no memory edit. The old incomplete-target discrepancy is resolved by the approved singleton-preservation contract; no symvision recipe exists. Outer epic bob-cli-gm remains in progress for its other phases.

## Dependencies

- **Blocks:** [bob-cli-gm.2](bob-cli-gm.2.md) ✓ · ⧖ 2026-11-03
- **Blocks:** [bob-cli-gm.3](bob-cli-gm.3.md) ✓ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-gm.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-gm.1.md) | [bob-cli-gm.1](bob-cli-gm.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-gm.1.1.2][1] | Need this phase's notes and the approved outer epic decisions | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gm.1.1.2/README.md

<!-- sase:referenced-by:end -->
