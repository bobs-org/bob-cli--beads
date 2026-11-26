# Bead: bob-cli-qp.1 — bob props reference roles and the Reference contract

[Bead Pages](../README.md) / [bob-cli-qp](README.md) / bob-cli-qp.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.6l.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.6l.linker.w0.md) · **Assignee:** `bob-cli-qp.1` · **Size:** medium
**Created:** 2026-11-26 14:22:07 EST · **Closed:** 2026-11-26 16:09:15 EST
**Plan:** [202611/ref\_cards.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/ref_cards.md)

## Description

ref-props: scope the reference note kind to bob's library coverage, protect sync, identity, and reading-task keys (resolving bob-cli-qn), and add the bob-owned reference settings contract. It also adds the props_ref_contract_v1 capability and the conditional H1 retitle, with docs and tests.

## Notes

[2026-11-26T21:08:55Z · bob-cli-qp.1--1] PROPOSED FOLLOW-UP: include note_kind in props update JSON reports — tests/cli/props_contract.rs::update_json_returns_candidate_contract_after_clear_apply_and_undo expects bank_preview.note_kind to be "bank", but update_report_json omits note_kind in the clean base; this was the sole failure in the final just check.

[2026-11-26T21:09:15Z · bob-cli-qp.1--1] Implemented the Reference props contract, reference-scoped roles and protected keys, reversible matching-H1 retitle, docs, and tests. Focused props and reference CLI checks plus docs-check passed; final just check found only the clean-base update JSON note_kind mismatch, recorded above as a proposed follow-up. Epic-symbol gate is clear.

## Dependencies

- **Blocks:** [bob-cli-qp.6](bob-cli-qp.6.md) ◐ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-qp.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-qp.1.md) | [bob-cli-qp.1](bob-cli-qp.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-qp.1--1][1] | Need the phase scope, prior notes, and assigned bead status before finalizing | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-qp.1.md

<!-- sase:referenced-by:end -->
