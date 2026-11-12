# Bead: bob-cli-kd.4.1.2 — Plan only missing rows and preserve existing writing

[Bead Pages](../README.md) / [bob-cli-kd.4.1](bob-cli-kd.4.1.md) / bob-cli-kd.4.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-kd.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kd.4.md) · **Assignee:** `bob-cli-kd.4.1.2` · **Size:** medium
**Created:** 2026-11-11 14:24:04 EST · **Closed:** 2026-11-11 16:36:42 EST
**Plan:** [202611/bank\_import.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_import.md)

## Description

match-name-plan: build a pure whole-batch planner for seen identities, typed-row matching, learned and configured naming, restaurant links, month edits, and journal events, with exact deterministic previews.

## Notes

[2026-11-11T21:36:15Z · bob-cli-kd.4.1.2] PROPOSED FOLLOW-UP: complete_themes shell-completion tests (theme_recent_shell_description_and_quoted_replacement, configured_shell_describes_never_used_and_unconfigured_create) fail under default-parallel full cli-suite runs but pass isolated and at --test-threads=8; clean tree fails identically. Already tracked by bob-cli-g8.

[2026-11-11T21:36:20Z · bob-cli-kd.4.1.2] PROPOSED FOLLOW-UP: just check clippy gate fails at src/native/vault_git.rs:65 items_after_test_module on an untouched file; clean tree fails identically. Already noted on bob-cli-kd.4.1.1.

[2026-11-11T21:36:42Z · bob-cli-kd.4.1.2] match-name-plan done: naming.rs (cleaning, 4-tier naming, payee sanitize) + import_plan.rs (pure whole-batch planner: seen/recovery/before-start/typed-match/ambiguous/new dispositions, ID reservation with 8→12 extension, ordered journal events, month before/after images, read deps, duplicate/conflict/malformed findings, affected rows[]). Row origin now reports matched journal outcomes with imported fallback. Verified: cargo test --lib 6626 passed incl 33 new planner/naming tests; my files fmt+clippy clean; full cli suite 3564+2 pre-existing parallel flakes (tracked by bob-cli-g8, reproduce on clean tree); just-check clippy gate blocked only by pre-existing vault_git.rs:65 (noted on kd.4.1.1). Public planner APIs for kd.4.1.3/kd.5: plan_batch, PlanInput, BatchPlan, PlanRefusal, Naming via resolve_name/clean_description/sanitize_payee, ReadDep, RestaurantEntry.

## Dependencies

- **Depends on:** [bob-cli-kd.4.1.1](bob-cli-kd.4.1.1.md) ✓ · ⧖ 2026-11-11
- **Blocks:** [bob-cli-kd.4.1.3](bob-cli-kd.4.1.3.md) ✓ · ⧖ 2026-11-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kd.4.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.4.1.2/README.md) | [bob-cli-kd.4.1.2](bob-cli-kd.4.1.2.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kd.4.1.2][1] | check notes/decisions | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.4.1.2/README.md

<!-- sase:referenced-by:end -->
