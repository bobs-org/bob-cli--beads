# Bead: bob-cli-c9.4.1.3 — Recover interrupted overwrites from host-local intents

[Bead Pages](../README.md) / [bob-cli-c9.4.1](bob-cli-c9.4.1.md) / bob-cli-c9.4.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-c9.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.4.md) · **Assignee:** `bob-cli-c9.4.1.3` · **Size:** medium
**Created:** 2026-10-25 22:34:44 EDT · **Closed:** 2026-10-25 23:28:45 EDT
**Plan:** [202610/unannotated\_reference\_overwrite.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/unannotated_reference_overwrite.md)

## Description

recovery: implement durable overwrite intents and scoped HEAD recovery before create or scan can sync; preserve dry-run and JSON contracts and test interrupted and committed states.

## Notes

[2026-10-26T03:28:20Z · bob-cli-c9.4.1.3] PROPOSED FOLLOW-UP: capture_related synthetic_vault_query_is_under_250ms flakes under parallel load (took 515ms vs 250ms budget in cargo test --lib, passes in isolation and in full cargo test runs); consider raising the load-absorbing budget or quarantining the timing assertion

[2026-10-26T03:28:45Z · bob-cli-c9.4.1.3] Implemented durable overwrite-intent lifecycle in highlights_ref/overwrite/recovery.rs with entry hooks in create.rs, sync.rs, scan_json.rs, and intake.rs (drain_queue covers both intake-only variants). Recovery: committed-proof via recorded SHA+subject+ancestry (generic subject match alone insufficient), scoped checkout/remove/unstage from clean locked HEAD, dry-run read-only refusal with recovery_required JSON code, idempotent retry with marker preserved on failure, path validation rejects escapes and .git roots. Verified: 12 new lib unit tests on isolated git fixtures, 4 new CLI fixture tests (tests/cli/highlights/overwrite_recovery.rs), highlights CLI 449 pass, ref_library CLI 143 pass, full cargo test --no-fail-fast green (3520 lib + 2136 cli), cargo fmt clean, clippy gate exit 0. Timing flake in capture_related 250ms test filed as PROPOSED FOLLOW-UP; passes in isolation and full runs.

## Dependencies

- **Depends on:** [bob-cli-c9.4.1.1](bob-cli-c9.4.1.1.md) ✓ · ⧖ 2026-10-25
- **Blocks:** [bob-cli-c9.4.1.4](bob-cli-c9.4.1.4.md) ✓ · ⧖ 2026-10-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-c9.4.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.4.1.3/README.md) | [bob-cli-c9.4.1.3](bob-cli-c9.4.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`07d5a18`](https://github.com/bobs-org/bob-cli/commit/07d5a18d1057e337a969e71741bc756a964c519f) | feat(highlights-ref): durable overwrite-intent lifecycle with recovery | [bob-cli-c9.4.1.3](bob-cli-c9.4.1.3.md) | 2026-10-25 23:29:51 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-c9.4.1.3][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.4.1.3/README.md

<!-- sase:referenced-by:end -->
