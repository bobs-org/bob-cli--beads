# Bead: bob-cli-on.11.1.2 — Port requirement close snapshots and verdict validation

[Bead Pages](../README.md) / [bob-cli-on.11.1](bob-cli-on.11.1.md) / bob-cli-on.11.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-on.11](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.11.md) · **Assignee:** `bob-cli-on.11.1.2` · **Size:** medium
**Created:** 2026-11-22 14:59:30 EST · **Closed:** 2026-11-22 15:23:05 EST
**Plan:** [202611/obsidian\_requirement\_close\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/obsidian_requirement_close_card.md)

## Description

req_model: add pure requirement group, identity, choice, fold, and stale-validation twins pinned to RV1-RV19, with copies for navigation and the cycler.

## Notes

[2026-11-22T20:22:53Z · bob-cli-on.11.1.2] PROPOSED FOLLOW-UP: npm test unit flake in scripts/test-ledger-tools-frees-marks.cjs ("200-link / 2000-task build stays within the 25 ms budget", synthetic build took 58 ms) under parallel suite load; isolated rerun passes; already tracked by bob-cli-io

[2026-11-22T20:23:05Z · bob-cli-on.11.1.2] Ported req_close.rs + req_verdicts.rs into cycler twins 198a/198b (copy, collect, numbering, fold, overlap, stale, pin) with byte-identical nav copies 699/699a; copied tests/fixtures/req_close byte-for-byte; RV1–RV19+RV44+copy+injected-snapshot+twin-copy 33/33; build:check and docs:inventory:check pass; deployed task-status-cycler and bob-navigation-hotkeys via landed inclusion proof f74c45e then dirty descendant sync (no -F). npm test had one unrelated frees-marks 25ms flake (bob-cli-io); isolated rerun passes. Live picker/API not advertised; Block ID Prompt stays RQ-only.

## Dependencies

- **Blocks:** [bob-cli-on.11.1.3](bob-cli-on.11.1.3.md) ✓ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-on.11.1.4](bob-cli-on.11.1.4.md) ✓ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.11.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.11.1.2/README.md) | [bob-cli-on.11.1.2](bob-cli-on.11.1.2.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-on.11.1.2][1] | Need the phase scope, notes, and design file before continuing remaining verify work | 5 |
| read-by | [agent:bob-cli-on.11.1.4][2] | Need req_model completion note and helper contract | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.11.1.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.11.1.4/README.md

<!-- sase:referenced-by:end -->
