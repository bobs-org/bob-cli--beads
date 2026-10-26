# Bead: bob-cli-c9.5.1.3 — Recover transactions that renamed annotated bundles

[Bead Pages](../README.md) / [bob-cli-c9.5.1](bob-cli-c9.5.1.md) / bob-cli-c9.5.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-c9.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.5.md) · **Assignee:** `bob-cli-c9.5.1.3` · **Size:** medium
**Created:** 2026-10-26 07:41:50 EDT · **Closed:** 2026-10-26 08:54:36 EDT
**Plan:** [202610/annotated\_reference\_overwrite.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/annotated_reference_overwrite.md)

## Description

recovery: Extend the host-local overwrite intent and recovery to describe no-clobber PDF and asset moves, reverse them safely on failure, and preserve unexpected late editor writes. Retain version-1 intent compatibility. Keep production annotated overwrite disabled; exercise recovery with synthetic interrupted transactions.

## Notes

[2026-10-26T12:54:24Z · bob-cli-c9.5.1.3] PROPOSED FOLLOW-UP: capture_related synthetic-vault 250ms lib perf gates flaked under parallel full-suite load (1220ms+); isolated runs pass on base and patched trees; already tracked by bob-cli-ca

[2026-10-26T12:54:36Z · bob-cli-c9.5.1.3] Implemented schema-v2 move-aware overwrite recovery in overwrite/recovery.rs (moves, writes, coordinated no-clobber reversal, fail-closed ownership). Verified: 28 recovery unit tests, 871 highlights_ref lib tests, 71 overwrite CLI tests incl. new scan-level v2 reversal test pass; fmt and clippy gate clean; production annotated overwrite still refused. Full lib suite: only known bob-cli-ca timing flake (passes isolated on base and patched trees).

## Dependencies

- **Depends on:** [bob-cli-c9.5.1.1](bob-cli-c9.5.1.1.md) ✓ · ⧖ 2026-10-26
- **Blocks:** [bob-cli-c9.5.1.4](bob-cli-c9.5.1.4.md) ✓ · ⧖ 2026-10-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-c9.5.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.5.1.3/README.md) | [bob-cli-c9.5.1.3](bob-cli-c9.5.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`564168f`](https://github.com/bobs-org/bob-cli/commit/564168f3a8c29d7bb55a5009d0906a27bf1a497c) | feat(ref): recover annotated overwrite transactions that renamed bundles | [bob-cli-c9.5.1.3](bob-cli-c9.5.1.3.md) | 2026-10-26 08:55:40 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-c9.5.1.3][1] | Need the phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.5.1.3/README.md

<!-- sase:referenced-by:end -->
