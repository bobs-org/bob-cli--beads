# Bead: bob-cli-hn.6.1.1 — Repair the shared offer-close contract and executable vectors

[Bead Pages](../README.md) / [bob-cli-hn.6.1](bob-cli-hn.6.1.md) / bob-cli-hn.6.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-hn.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hn.6.md) · **Assignee:** `bob-cli-hn.6.1.1` · **Size:** medium
**Created:** 2026-11-05 20:37:46 EST · **Closed:** 2026-11-05 21:22:42 EST
**Plan:** [202611/cycler\_offer\_verdicts.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/cycler_offer_verdicts.md)

## Description

contract_parity: align the landed Rust descriptor copy and shared SV fixtures with the approved parent design, make the engine vectors executable, and preserve existing close bytes and recovery policy.

## Notes

[2026-11-06T02:22:23Z · bob-cli-hn.6.1.1] PROPOSED FOLLOW-UP: just check blocked by pre-existing unused const TODAY in tests/cli/capture/merge_in.rs:8 (touches no contract_parity file; fails identically on clean base)

[2026-11-06T02:22:27Z · bob-cli-hn.6.1.1] PROPOSED FOLLOW-UP: cargo test --lib has 2 pre-existing clean-base failures (completion kinds duplicate clipboard:count; catalog clipboard in both lists) matching hn.2 clipboard-registration tracking; offer_close 10/10 pass

[2026-11-06T02:22:32Z · bob-cli-hn.6.1.1] PROPOSED FOLLOW-UP: just docs-check lychee fails on clean base too (task-merge/index.html -> target/docs/capture#merging-tasks-into-a-new-task-with, File not found); unrelated to task-dependencies edits

[2026-11-06T02:22:42Z · bob-cli-hn.6.1.1] contract_parity done: Rust descriptor uses canonical why/consequence/scope/unblock-tickler copy with OfferCloseRefusal separated from display text; vectors.json fixed (SV9/SV10 fresh, SV8 refusal+why, new SV17-SV22) and executable in offer_close_tests (10/10 pass); docs 12.5/12.22-12.23 aligned to parent canonical table. Gates: cargo fmt pass, clippy pass on touched files, cargo test --lib offer_close 10/10, full lib 5261 pass with 2 known clipboard failures, docs-check lychee failure reproduces on clean base

## Dependencies

- **Blocks:** [bob-cli-hn.6.1.2](bob-cli-hn.6.1.2.md) ✓ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-hn.6.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hn.6.1.1/README.md) | [bob-cli-hn.6.1.1](bob-cli-hn.6.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`44c5c8c`](https://github.com/bobs-org/bob-cli/commit/44c5c8c8fd44340dcfb7376fcd13464032131ee1) | fix(capture): repair shared offer-close contract and executable vectors | [bob-cli-hn.6.1.1](bob-cli-hn.6.1.1.md) | 2026-11-05 21:24:04 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hg.6.1.1--1][1] | Need the existing task note about clean-base check failures | 1 |
| read-by | [agent:bob-cli-hn.6.1.1][2] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hg.6.1.1.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hn.6.1.1/README.md

<!-- sase:referenced-by:end -->
