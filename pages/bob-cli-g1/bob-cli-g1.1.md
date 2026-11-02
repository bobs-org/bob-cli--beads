# Bead: bob-cli-g1.1 — Authoritative display contract (bob-cli)

[Bead Pages](../README.md) / [bob-cli-g1](README.md) / bob-cli-g1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.176](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.176.md) · **Assignee:** `bob-cli-g1.1` · **Size:** small
**Created:** 2026-11-02 12:45:29 EST · **Closed:** 2026-11-02 12:57:54 EST
**Plan:** [202611/ledger\_frees\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/ledger_frees_marks.md)

## Description

contract: write and register bob-cli docs/frees-marks.md (rule, look, placement, tooltip, motion, liveness, FL/FC/FT/FP vectors) and cross-link BLOCKS §14.9.

## Notes

[2026-11-02T17:57:54Z · bob-cli-g1.1] Wrote and registered docs/frees-marks.md (compact pill_text: pill reads 🔑 N) with rule, look, placement, tooltip, motion, liveness, FL/FC/FT/FP vectors, JS mirror file names, no api namespace; cross-linked BLOCKS §14.9 Ledger echo; ran just docs-gen then just docs-check until all 447 tests passed (bumped registry count 33→34 and README snapshot in tools/docs/tests/test_contracts.py); committed c4411f64 without touching Cargo.toml/CHANGELOG.md; no epic symbols.

## Dependencies

- **Blocks:** [bob-cli-g1.2](bob-cli-g1.2.md) ✓ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-g1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-g1.1/README.md) | [bob-cli-g1.1](bob-cli-g1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b508f0b`](https://github.com/bobs-org/bob-cli/commit/b508f0b69dbd5dab08b7e6d1eb7c4c0f2ae1a01a) | docs(frees-marks): add ledger frees-mark display contract | [bob-cli-g1.1](bob-cli-g1.1.md) | 2026-11-02 12:58:52 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-g1.1][1] | Need the phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-g1.1/README.md

<!-- sase:referenced-by:end -->
