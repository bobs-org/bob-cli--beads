# Bead: bob-cli-ls.2.1 — Subscription registry, attribution, and ledger core

[Bead Pages](../README.md) / [bob-cli-ls.2](bob-cli-ls.2.md) / bob-cli-ls.2.1

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-ls.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ls.2.md) · **Assignee:** `bob-cli-ls.2.1.land`
**Created:** 2026-11-15 13:23:48 EST
**Plan:** [202611/subscription\_core.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/subscription_core.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/subscription_core.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/subscription_core.md

<!-- sase:links:end -->

## Description

Complete bob-cli-ls.2 with one reusable subscription resolver and ledger, guarded registry inputs, and additive bank row JSON.

## Notes

[2026-11-15T21:00:06Z · bob-cli-lr.land] DISCOVERED ISSUE (found by the bob-cli-lr land agent, 2026-11-15): on origin/master d794e0ba, just check fails in the clippy step (-D unused) on the subscription registry from c59b5b80 (bob-cli-ls.2.1.1), which nothing calls yet. Errors: unused import RecordField (src/native/bank/subscriptions/registry.rs:19); unused re-exports resolve_match/SubscriptionMatch and parse_subscription_snapshot/Subscription* (src/native/bank/subscriptions/mod.rs:6-11); never-used SubscriptionStatus::is_cancelled (registry.rs:93), SubscriptionCadence::as_str (registry.rs:107), and SubscriptionPricing::as_str (registry.rs:124). cargo test still compiles and passes. Impact: every other agent's just check fails at clippy until this epic wires the registry up (ls.2.1.2 is closed but has no commit on master yet; ls.2.1.3 is in progress), or the symbols get a temporary allow.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ls.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ls.2.1.land/README.md) | [bob-cli-ls.2.1](bob-cli-ls.2.1.md) | 0 |
