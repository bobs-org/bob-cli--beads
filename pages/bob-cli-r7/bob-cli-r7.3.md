# Bead: bob-cli-r7.3 — Stable frees-marks 25 ms CPU budget measurement

[Bead Pages](../README.md) / [bob-cli-r7](README.md) / bob-cli-r7.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1h4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1h4.md) · **Assignee:** `bob-cli-r7.3` · **Size:** medium
**Created:** 2026-11-27 10:16:12 EST · **Closed:** 2026-11-27 11:33:39 EST
**Plan:** [202611/task\_bead\_burndown\_1.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_bead_burndown_1.md)

## Description

frees-marks-budget: replace the single cold CPU sample in the bob-plugins frees-marks 200-link/2000-task gate with the warm best-of-N pattern that fixed sibling gates, keep the 25 ms target, then close bob-cli-io.

## Notes

[2026-11-27T16:33:15Z · bob-cli-r7.3] PROPOSED FOLLOW-UP: bob-plugins full npm test fails test-snooze-model-vectors.cjs node "navigation runs all canonical snooze add and drop mutation vectors" (snooze-add-resnooze-replaces-history daily postimage whitespace mismatch) on the clean base tree without this phase change; track as a new task bead at land time

[2026-11-27T16:33:39Z · bob-cli-r7.3] bob-plugins 360dc776 replaces the single cold CPU sample in the frees-marks 200-link/2000-task gate with the shared warm best-of-7 pattern (25 ms target kept). Verified: focused file 17/17; three consecutive full npm test runs pass the node (ok 2238) with the only failure the pre-existing snooze mutation-vectors node, proven identical on the clean base and recorded as PROPOSED FOLLOW-UP. Did not run bob plugins sync: vault bob-ledger-tools deploy belongs to still-running ws17 agent 1h7--1 and this change is test-only (no bundle change), so no -F per linked-repo AGENTS.md.

## Dependencies

- **Depends on:** [bob-cli-r7.2](bob-cli-r7.2.md) ✓ · ⧖ 2026-11-27
- **Blocks:** [bob-cli-r7.4](bob-cli-r7.4.md) ◐ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-r7.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-r7.3/README.md) | [bob-cli-r7.3](bob-cli-r7.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@738ad52`](https://github.com/bobs-org/bob-plugins/commit/738ad5293c04856c69ff23ab919213197c11857a) | test(ledger-tools): stabilize frees-marks 25ms budget with warm best-of-7 CPU sampling | [bob-cli-r7.3](bob-cli-r7.3.md) | 2026-11-27 11:35:25 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-r7.3][1] | Confirm phase close landed | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-r7.3/README.md

<!-- sase:referenced-by:end -->
