# Bead: bob-cli-pl.9.1.2.1.1 — Make Bank acceptance probes match the production contract

[Bead Pages](../README.md) / [bob-cli-pl.9.1.2.1](bob-cli-pl.9.1.2.1.md) / bob-cli-pl.9.1.2.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pl.9.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pl.9.1.2.md) · **Assignee:** `bob-cli-pl.9.1.2.1.1` · **Size:** medium
**Created:** 2026-11-26 03:28:46 EST · **Closed:** 2026-11-26 05:42:15 EST
**Plan:** [202611/bank\_area\_arbitration\_repair.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_area_arbitration_repair.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:6fed67657bdc3c6424a2728b | attached via sase artifact create --bead |
| related | file:explicit:fe0b22b0a0295a7a7901d2c1 | attached via sase artifact create --bead |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

bank-probe-contracts: isolate a complete bank acceptance slice, repair report/modal assumptions, and retain independent failure evidence without masking ownership defects.

## Notes

[2026-11-26T10:42:15Z · bob-cli-pl.9.1.2.1.1--5] Evidence capture complete; this is not product acceptance. Focused offline tests: 17 passed, 0 failed. Athena report: NO-GO, pass=false (14 of 29 checks passed; 15 failed; 35 skipped). Final invariants: all 20 fixture hashes expected=seeded=final, zero watcher transitions, bytes-unchanged passed, empty vault write audit, zero console exceptions/errors. All eight screenshots were individually reviewed; verdicts, dimensions, and SHA-256 values are in the attached archive. CLI source 8cb474ba818f1e214e38634dce63f8ffb120b11d and plugin source b9b3cec922189b7bb068b2d4c5b072b9fb8d0500 were verified; input inventories 2615 CLI files and 1977 plugin files and all 13 output payload checksums pass. Raw report: file:explicit:6fed67657bdc3c6424a2728b. Complete evidence archive: file:explicit:fe0b22b0a0295a7a7901d2c1. Failed probe details remain in the raw report; no product acceptance is claimed.

## Dependencies

- **Blocks:** [bob-cli-pl.9.1.2.1.2](bob-cli-pl.9.1.2.1.2.md) ✓ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pl.9.1.2.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pl.9.1.2.1.1.md) | [bob-cli-pl.9.1.2.1.1](bob-cli-pl.9.1.2.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@072b009`](https://github.com/bobs-org/bob-plugins/commit/072b009e91820b51d1bbebb3ef0abe06e7f28d75) | test(acceptance): add Bank-only Obsidian acceptance profile | [bob-cli-pl.9.1.2.1.1](bob-cli-pl.9.1.2.1.1.md) | 2026-11-26 04:10:50 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pl.9.1.2.1.2][1] | Need prior phase deliverable and harness contract | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pl.9.1.2.1.2/README.md

<!-- sase:referenced-by:end -->
