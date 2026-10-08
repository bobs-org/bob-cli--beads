# Bead: bob-cli-5p.2 — bob-ledger-tools evaluator, footer, and freshness namespace v9

[Bead Pages](../README.md) / [bob-cli-5p](README.md) / bob-cli-5p.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0yb](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0yb.md) · **Assignee:** `bob-cli-5p.2` · **Size:** medium
**Created:** 2026-10-08 11:03:15 EDT · **Closed:** 2026-10-08 11:38:07 EDT
**Plan:** [202610/recurring\_review\_tier.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/recurring_review_tier.md)

## Description

ledger: mirror the RECURRING overlay, ordering, and counts in bob-ledger-tools, add the RECUR footer group and entry view, publish freshness namespace v9 with recurringTier, and pin the RC vectors in JS tests.

## Notes

[2026-10-08T15:37:55Z · bob-cli-5p.2] PROPOSED FOLLOW-UP: nav roll-decay picker-single P2 tests fail identically on clean base (test-navigation-roll-decay.cjs: expected [?] got [ ]); pre-existing, unrelated to ledger RECURRING work

[2026-10-08T15:37:59Z · bob-cli-5p.2] PROPOSED FOLLOW-UP: per epic memory_records=no decision, consider adding a RECURRING-tier decision record, marking decisions:review-walk-is-tiered superseded in part, and editing glossary:task-freshness

[2026-10-08T15:38:07Z · bob-cli-5p.2] Ledger RECURRING tier done: evaluator overlay (occurs_on, tier/order/counts), due/start rows, RECUR footer group + entry view + RECUR legend, marks tone/tooltip, namespace v9 recurringTier, manifest 1.36.0, README. Verified: 193/193 freshness tests pass (incl. 17 new RC1-RC12), build:check + validate clean, bob plugins sync deployed. 2 nav roll-decay failures reproduce identically on clean base (recorded as follow-up).

## Dependencies

- **Depends on:** [bob-cli-5p.1](bob-cli-5p.1.md) ✓ · ⧖ 2026-10-08
- **Blocks:** [bob-cli-5p.3](bob-cli-5p.3.md) ◐ · ⧖ 2026-10-08
- **Blocks:** [bob-cli-5p.4](bob-cli-5p.4.md) ◐ · ⧖ 2026-10-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-5p.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5p.2/README.md) | [bob-cli-5p.2](bob-cli-5p.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@9233b0c`](https://github.com/bobs-org/bob-plugins/commit/9233b0cb717b3d09ba2de3da60a1eeb4528e4a22) | feat(ledger-tools): add RECURRING freshness tier with overlay, queue and footer | [bob-cli-5p.2](bob-cli-5p.2.md) | 2026-10-08 11:39:17 EDT |
