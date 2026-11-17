# Bead: bob-cli-mr.1 — Fix the deterministic bob-plugins npm test reds

[Bead Pages](../README.md) / [bob-cli-mr](README.md) / bob-cli-mr.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1dh](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1dh.md) · **Assignee:** `bob-cli-mr.1` · **Size:** medium
**Created:** 2026-11-17 11:16:43 EST · **Closed:** 2026-11-17 11:31:04 EST
**Plan:** [202611/backlog\_triage\_t1\_red\_gates\_closed\_prereqs\_scan\_lock.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/backlog_triage_t1_red_gates_closed_prereqs_scan_lock.md)

## Description

plugin-reds: update the stale walkMode v5 and hex-guard pins (bob-cli-md), stop Platform shadowing from breaking platform tests (bob-cli-me), defuse the block-marks fixture date bomb (bob-cli-m8), and close all three.

## Notes

[2026-11-17T16:30:26Z · bob-cli-mr.1] Full npm test after fixes (bob-plugins b0a9c89, 7183 tests): only reds are already-tracked load flakes. Run 1: off-clock-link-chips 200-link node 41.3ms vs 25ms (bob-cli-ju; 56/56 isolated). Run 2: same ju node 123.9ms + keep-moving-marks-surface 200-link node 1306ms vs 250ms (bob-cli-ki). Varies run to run; files untouched by this phase. All md/me/m8 nodes green in-suite.

[2026-11-17T16:31:04Z · bob-cli-mr.1] All three reds fixed in bob-plugins b0a9c89 (pushed, master in sync) and md/me/m8 closed with test evidence. No --epic-symbol entries remain. Only full-suite reds are the tracked ju/ki load flakes, named in the phase notes.

## Dependencies

- **Blocks:** [bob-cli-mr.2](bob-cli-mr.2.md) ✓ · ⧖ 2026-11-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-mr.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-mr.1/README.md) | [bob-cli-mr.1](bob-cli-mr.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-mr.1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-mr.1/README.md

<!-- sase:referenced-by:end -->
