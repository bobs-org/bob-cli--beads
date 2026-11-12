# Bead: bob-cli-k3.10 — Link the spending ledger to restaurant records and backfill visited

[Bead Pages](../README.md) / [bob-cli-k3](README.md) / bob-cli-k3.10

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** `bbugyi200.apollo.research.43.linker.w0` · **Assignee:** `bob-cli-k3.10` · **Size:** medium
**Created:** 2026-11-11 04:56:44 EST
**Plan:** [202611/album\_and\_record\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/album_and_record_notes.md)

## Description

ledger-mining: when accepted, rewrite the 653 mappable `[[eat#<lid>]]` spending links in historical `_habit.md` notes to their records and backfill each restaurant's `visited` from its latest ledger date in one reviewed commit; otherwise close as a no-op.

## Dependencies

- **Blocks:** [bob-cli-k3.11](bob-cli-k3.11.md) ◐ · ⧖ 2026-11-11
- **Depends on:** [bob-cli-k3.9](bob-cli-k3.9.md) ✓ · ⧖ 2026-11-11

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:research.47.gem][1] | check spending ledger context | 1 |
| read-by | [agent:research.47.mus][2] | Need spending ledger linking details for bank album research | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.47.gem/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.47.mus/README.md

<!-- sase:referenced-by:end -->
