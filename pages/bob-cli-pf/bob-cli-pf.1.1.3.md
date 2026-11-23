# Bead: bob-cli-pf.1.1.3 — Album, temporal, and bank foot adoption

[Bead Pages](../README.md) / [bob-cli-pf.1.1](bob-cli-pf.1.1.md) / bob-cli-pf.1.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pf.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.1.md) · **Assignee:** `bob-cli-pf.1.1.3` · **Size:** medium
**Created:** 2026-11-22 14:45:09 EST · **Closed:** 2026-11-22 17:50:50 EST
**Plan:** [202611/card\_foot\_drawer.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/card_foot_drawer.md)

## Description

adapters: adopt the shared foot after each rail on album, day, week, quarter, year, and bank setup cards, including identity-only and collapsed states, with focused tests and species documentation.

## Notes

[2026-11-22T22:50:50Z · bob-cli-pf.1.1.3] Album, day/week/quarter/year, and bank setup cards adopt the shared property-card foot after each rail. Shared 240r adapter plus 241va/248ca/296da mixins; identity-only and collapsed bank states keep the foot; native own-keys unchanged; adapter unbind uses ReleasePath not reset-all. Verified: node --test of adapters + title-block + album-header + bank-setup + property-card-foot + record-sheet = 178 pass; npm run build:check; npm run docs:check (447 pass, 1 skip, bank copy under 6000-word cap); docs:inventory:check; epic-symbols none leftover; bob plugins sync deployed ledger-tools.

## Dependencies

- **Depends on:** [bob-cli-pf.1.1.2](bob-cli-pf.1.1.2.md) ✓ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-pf.1.1.4](bob-cli-pf.1.1.4.md) ✓ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pf.1.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.1.1.3/README.md) | [bob-cli-pf.1.1.3](bob-cli-pf.1.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@b3188ab`](https://github.com/bobs-org/bob-plugins/commit/b3188ab5be762a75786f51e2ed9e10f2063f2cc7) | feat(ledger-tools): adopt shared property-card foot on album, temporal, and bank cards | [bob-cli-pf.1.1.3](bob-cli-pf.1.1.3.md) | 2026-11-22 17:52:22 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pf.1.1.3][1] | Need the phase scope, design file, notes, and epic decisions | 7 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.1.1.3/README.md

<!-- sase:referenced-by:end -->
