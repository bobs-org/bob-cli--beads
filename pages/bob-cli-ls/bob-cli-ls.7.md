# Bead: bob-cli-ls.7 — 🔁 chips on bank rows

[Bead Pages](../README.md) / [bob-cli-ls](README.md) / bob-cli-ls.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1cp](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1cp.md) · **Assignee:** `bob-cli-ls.7` · **Size:** medium
**Created:** 2026-11-15 13:11:22 EST · **Closed:** 2026-11-15 18:29:46 EST
**Plan:** [202611/bank\_subscriptions\_album.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_subscriptions_album.md)

## Description

chips: render subscription links as state-aware 🔁 pills in Live Preview, Reading view, and the queue card, with tooltips, ghost chips, and click-to-link.

## Notes

[2026-11-15T23:29:15Z · bob-cli-ls.7] PROPOSED FOLLOW-UP: npm run docs:check still fails on mounted docs/reference/plugins/bob-ledger-tools.md word budget (HEAD 6055, this phase 6142, cap 6000) — already tracked by bob-cli-il; chip docs were condensed to 87 words so the overage is the pre-existing Setup-header overrun plus required chip contract copy.

[2026-11-15T23:29:28Z · bob-cli-ls.7] PROPOSED FOLLOW-UP: full bob-plugins npm test flakes three 25ms Live Preview budgets under parallel node --test (event-link-times 62ms, keep-moving-marks-surface 1485ms, off-clock-link-chips 143ms) that pass in isolation (9.3ms / 81.8ms / 8.4ms) — already tracked by bob-cli-km, bob-cli-ki, and bob-cli-ju.

[2026-11-15T23:29:46Z · bob-cli-ls.7] Painted state-aware 🔁 chips in bob-ledger-tools Live Preview (241p replace/ghost widgets), Reading view (241q wrap/append + restore of .is-appended), and the queue card (after category). Decoder accepts subscription/bank_recurring/subscription_candidate plus suggestion source=subscription; older bob rows stay unchipped. Ghost click inserts [[subscriptions/<stem>|🔁]] as one editor transaction; to_cancel opens Manage url then the record; candidate click is a stub for linker. Targeted unit tests 56/56 pass (subscription/marks/cards/category). bob plugins sync deployed ledger-tools. No leftover --epic-symbol entries. docs:check still over budget (HEAD 6055, now 6142, cap 6000) tracked by bob-cli-il; three parallel-suite 25ms flakes pass isolated (bob-cli-km/ki/ju).

## Dependencies

- **Depends on:** [bob-cli-ls.2](bob-cli-ls.2.md) ✓ · ⧖ 2026-11-15
- **Blocks:** [bob-cli-ls.8](bob-cli-ls.8.md) ◐ · ⧖ 2026-11-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ls.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ls.7/README.md) | [bob-cli-ls.7](bob-cli-ls.7.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ls.7][1] | Need the phase scope and design file | 5 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ls.7/README.md

<!-- sase:referenced-by:end -->
