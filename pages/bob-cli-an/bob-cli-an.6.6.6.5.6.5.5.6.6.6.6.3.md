# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.3 — Make failing FakeNode asserts in ledger-tools suites report instead of OOM

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.3` · **Size:** small
**Created:** 2026-10-26 08:32:07 EDT · **Closed:** 2026-10-26 08:47:33 EDT
**Plan:** [202610/backlog\_batch12\_perf\_baseline\_fakenode\_daystrip\_blocks\_notice.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch12_perf_baseline_fakenode_daystrip_blocks_notice.md)

## Description

fakenode-inspect: resolve bob-cli-c7 by giving every bob-plugins ledger-tools test FakeNode a short util.inspect.custom descriptor, restoring the plan-host identity asserts, and adding a bounded-time failing-assert regression.

## Notes

[2026-10-26T12:47:22Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.3] PROPOSED FOLLOW-UP: day-strip follow-up phases (c6 new-tab, c8 legend overflow) will add new DOM asserts on live FakeNodes — they must use the assert.ok(===) + nodeNote message form, never assert.equal/deepEqual on two live nodes, or the bob-cli-c7 heap OOM returns

[2026-10-26T12:47:33Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.3] Done in bob-plugins (test-only changes, no plugin source edits, no deploy). Added short util.inspect.custom descriptors (tag, classes, child count, 40-char text prefix) to all 11 cyclic FakeNode-style fakes across 9 ledger-tools suites (7x FakeNode, 2x MiniNode, 2x pomodoro Node) plus the new regression files. DEVIATION with evidence: the plan's 'convert identity checks back to assert.equal' step was NOT applied — on Node v22 assert's structural differ ignores inspect.custom and eagerly diffs even with a custom message, so assert.equal/deepEqual on the verbatim 85-node plan-host tree OOMs (exit 134, ~8s at 1024MB) with the descriptor grafted, without it, and with a custom message (probes in /tmp/verbatim*.log). Instead the 11 plan-host identity asserts keep the === form (which never diffs) via a nodeNote() helper whose util.inspect message names both nodes, e.g. failure reads '[FakeNode(DIV.bob-plan...) vs FakeNode(...)]'. New regression scripts/test-ledger-tools-fakenode-inspect.cjs (+child probe, wired into npm test): failing identity assert names both descriptors in ~2ms default heap and ~40ms under a 1024MB child cap, and asserts every suite file carries its descriptor(s). Verified: 11 touched suites 191/191 pass; npm test 3683/3683 pass; npm run validate exit 0. Target task bob-cli-c7 left open for the lander.

## Dependencies

- **Blocks:** [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.4](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.4.md) ✓ · ⧖ 2026-10-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.3/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.3](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.3.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.3][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.3/README.md

<!-- sase:referenced-by:end -->
