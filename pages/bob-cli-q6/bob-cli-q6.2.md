# Bead: bob-cli-q6.2 — Setup collapses by default and the folded card stays honest

[Bead Pages](../README.md) / [bob-cli-q6](README.md) / bob-cli-q6.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1g2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1g2.md) · **Assignee:** `bob-cli-q6.2` · **Size:** medium
**Created:** 2026-11-25 12:49:31 EST · **Closed:** 2026-11-25 16:25:27 EST
**Plan:** [202611/bank\_property\_card\_fold.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_property_card_fold.md)

## Description

bank-fold: bank Setup resolves through the fold helper (collapsed when healthy, self-opening and still toggleable when broken), gains the shared fold row with an attention chip, and fixes the gap tone, rule numbering, ids, and stale-notice placement.

## Notes

[2026-11-25T21:25:19Z · bob-cli-q6.2] PROPOSED FOLLOW-UP: docs:check lint still fails on reference word budgets (bob-ledger-tools ~6057/6000, bob-navigation-hotkeys ~6068/6000, plus plugin-apis warning); reproduces on the clean base tree (base ledger-tools already 6002/6000), so pre-existing and not caused by bank-fold.

[2026-11-25T21:25:27Z · bob-cli-q6.2] bank-fold landed: Setup folds by default via shared kit (collapsed healthy, self-opening broken, toggleable), fold row with attention chip, stale outside the fold, single rules numbering, unique live ids, bodyless static rows; gap=warn; unit 196 pass (bank-setup 47, fold/schema/album/foot/sheet), build:check clean, docs paragraph updated, bob plugins sync deployed bob-ledger-tools 1.164.0; docs:check lint failure pre-existing on base (recorded as follow-up); e2e _ round trip + invalid toggle + Reading command added to setup e2e (real-Obsidian run not possible in this turn).

## Dependencies

- **Depends on:** [bob-cli-q6.1](bob-cli-q6.1.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q6.3](bob-cli-q6.3.md) ✓ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q6.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q6.2/README.md) | [bob-cli-q6.2](bob-cli-q6.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@fbe5fd8`](https://github.com/bobs-org/bob-plugins/commit/fbe5fd864f9c2c5c78ed32fcf2a912661a75d06b) | feat(bob-ledger-tools): fold bank Setup by default with honest attention | [bob-cli-q6.2](bob-cli-q6.2.md) | 2026-11-25 16:27:05 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q6.2][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q6.2/README.md

<!-- sase:referenced-by:end -->
