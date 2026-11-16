# Bead: bob-cli-ls.2 — Subscription registry, match resolver, and ledger

[Bead Pages](../README.md) / [bob-cli-ls](README.md) / bob-cli-ls.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1cp](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1cp.md) · **Assignee:** `bob-cli-ls.2` · **Size:** large
**Created:** 2026-11-15 13:11:21 EST · **Closed:** 2026-11-15 17:54:09 EST
**Plan:** [202611/bank\_subscriptions\_album.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_subscriptions_album.md)

## Description

core: load subscription records, implement the Shows-up-as match contract and the single attribution resolver over rows and journal history, derive each record's ledger, and add subscription fields to bank row JSON.

## Notes

[2026-11-15T22:54:53Z · bob-cli-ls.2.1.land] Core phase complete via child epic bob-cli-ls.2.1: shared registry/match/attribution/ledger, guarded parent/root/folder inputs including absents, import after-state and source-free -F, checked money and signed cadence, additive row JSON. just check passed. just docs-check fails only on independent mounted plugin page bob-ledger-tools.md 6055 vs 6000 (bob-cli-lt.3 / bob-cli-il). epic-symbols empty. Follow-ups stay on bob-cli-g8 and bob-cli-lt.3/bob-cli-il. Outer bob-cli-ls and bob-cli-kt remain open.

## Dependencies

- **Blocks:** [bob-cli-ls.4](bob-cli-ls.4.md) ✓ · ⧖ 2026-11-15
- **Blocks:** [bob-cli-ls.5](bob-cli-ls.5.md) ✓ · ⧖ 2026-11-15
- **Blocks:** [bob-cli-ls.6](bob-cli-ls.6.md) ✓ · ⧖ 2026-11-15
- **Blocks:** [bob-cli-ls.7](bob-cli-ls.7.md) ✓ · ⧖ 2026-11-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ls.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ls.2.md) | [bob-cli-ls.2](bob-cli-ls.2.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-lr.land][1] | Check whether the in-flight subscription registry phase already knows its unwired code fails clippy -D unused on master | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-lr.land/README.md

<!-- sase:referenced-by:end -->
