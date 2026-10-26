# Bead: bob-cli-c9.4.1.8 — Verify overwrite preservation and crash recovery end to end

[Bead Pages](../README.md) / [bob-cli-c9.4.1](bob-cli-c9.4.1.md) / bob-cli-c9.4.1.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-c9.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.4.md) · **Assignee:** `bob-cli-c9.4.1.8` · **Size:** medium
**Created:** 2026-10-25 22:34:44 EDT · **Closed:** 2026-10-26 03:00:32 EDT
**Plan:** [202610/unannotated\_reference\_overwrite.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/unannotated_reference_overwrite.md)

## Description

acceptance: close cross-route acceptance gaps, prove archive inertness and recovery through CLI fixtures, remove temporary symbols, and run the full code and documentation gates for the child epic land agent.

## Notes

[2026-10-26T07:00:21Z · bob-cli-c9.4.1.8] PROPOSED FOLLOW-UP: just check lib flake synthetic_vault_draft_contract_is_under_250ms (587ms vs 500ms under parallel load) — already tracked by bob-cli-bo; passes in isolation; unrelated to overwrite acceptance

[2026-10-26T07:00:32Z · bob-cli-c9.4.1.8] Verified overwrite preservation and crash recovery end to end: cargo test --test cli highlights::overwrite 35 passed (same-day archives, empty sidecar removal, task identity/freshness/inbound links, frozen-note inertness across list/find/doctor, -o refusal, unrelated dirty/staged files, writing create and scan -i/-f json recovery, leftover committed intent then second overwrite). just docs-gen and just docs-check passed. sase bead epic-symbols reported no leftovers. Overwrite preflight ignores leftover unannotated sidecars so they are removed instead of refusing not_in_sync. just check failed only on native::capture_related::tests::synthetic_vault_draft_contract_is_under_250ms (587ms vs 500ms under parallel load; already tracked by bob-cli-bo; passes in isolation).

## Dependencies

- **Depends on:** [bob-cli-c9.4.1.7](bob-cli-c9.4.1.7.md) ✓ · ⧖ 2026-10-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-c9.4.1.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.4.1.8/README.md) | [bob-cli-c9.4.1.8](bob-cli-c9.4.1.8.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`94abe3d`](https://github.com/bobs-org/bob-cli/commit/94abe3d98061c8642c7b91d9975999afeeed269e) | test(highlights): verify overwrite preservation and crash recovery | [bob-cli-c9.4.1.8](bob-cli-c9.4.1.8.md) | 2026-10-26 03:01:15 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-c9.4.1.8][1] | Need the phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.4.1.8/README.md

<!-- sase:referenced-by:end -->
