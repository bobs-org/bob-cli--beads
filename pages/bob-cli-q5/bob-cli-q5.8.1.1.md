# Bead: bob-cli-q5.8.1.1 — Make wake notification ownership and revalidation explicit

[Bead Pages](../README.md) / [bob-cli-q5.8.1](bob-cli-q5.8.1.md) / bob-cli-q5.8.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.md) · **Assignee:** `bob-cli-q5.8.1.1` · **Size:** medium
**Created:** 2026-11-26 12:54:20 EST · **Closed:** 2026-11-26 14:21:21 EST
**Plan:** [202611/mac\_snooze\_wake\_notice.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_snooze_wake_notice.md)

## Description

notice-protocol: add the minimal additive bob-cli receipt and list fields needed to select one notification channel, negotiate compatibility, and verify that a receipt still refers to actionable woken tasks. Cover the channel matrix and stale history cases, and document the schema-1 additions.

## Notes

[2026-11-26T19:21:09Z · bob-cli-q5.8.1.1--3] PROPOSED FOLLOW-UP: Repair pre-existing full-check failures. Both the phase run and clean-base commit 8025ab3c257b77b188e3f31212e229462a69bfe8 fail the same meeting PDF text test (native::meetings::profile::tests::wispr_summary_renders_one_or_two_pages_with_stable_words, src/native/meetings/profile.rs:489) and properties JSON assertion (props::contract::update_json_returns_candidate_contract_after_clear_apply_and_undo, tests/cli/props_contract.rs:382; null vs bank). Both docs checks report stale generated plugin inventory in docs/bob-ledger-tools.md and docs/index.md. Evidence: phase monitor yaen3qe5gafg; clean-base monitor 8zp7wsa10tp9.

[2026-11-26T19:21:21Z · bob-cli-q5.8.1.1--3] Phase verification: cargo test --test cli snooze passed (79 tests). just check and just docs-check failed on the phase branch and reproduced on clean base 8025ab3c257b77b188e3f31212e229462a69bfe8. The same failures were recorded in phase monitor yaen3qe5gafg and clean-base monitor 8zp7wsa10tp9: meetings::profile::tests::wispr_summary_renders_one_or_two_pages_with_stable_words (profile.rs:489), props::contract::update_json_returns_candidate_contract_after_clear_apply_and_undo (props_contract.rs:382; null vs bank), and stale generated plugin inventory in docs/bob-ledger-tools.md and docs/index.md. A PROPOSED FOLLOW-UP note records these baseline issues.

## Dependencies

- **Blocks:** [bob-cli-q5.8.1.2](bob-cli-q5.8.1.2.md) ✓ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.8.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.1.1.md) | [bob-cli-q5.8.1.1](bob-cli-q5.8.1.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`3659edc`](https://github.com/bobs-org/bob-cli/commit/3659edc091409eed14ec8f0a316eedff400156bb) | feat(snooze): add wake notice ownership and eligibility fields | [bob-cli-q5.8.1.1](bob-cli-q5.8.1.1.md) | 2026-11-26 13:18:07 EST |
| bob-cli | [`59037b2`](https://github.com/bobs-org/bob-cli/commit/59037b2343f0b15cf7d98c5acdaf7223028e3d1c) | fix(snooze): correct test paths and anonymize vault example | [bob-cli-q5.8.1.1](bob-cli-q5.8.1.1.md) | 2026-11-26 14:06:20 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.8.1.1--2][1] | Need the assigned snooze phase scope and completion instruction | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.1.1.md

<!-- sase:referenced-by:end -->
