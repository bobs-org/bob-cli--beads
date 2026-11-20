# Bead: bob-cli-nh.6 — Property-card kit extracted from the album, record, and bank cards

[Bead Pages](../README.md) / [bob-cli-nh](README.md) / bob-cli-nh.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1ef](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1ef.md) · **Assignee:** `bob-cli-nh.6` · **Size:** large
**Created:** 2026-11-19 09:35:22 EST · **Closed:** 2026-11-19 18:10:20 EST
**Plan:** [202611/period\_intentions.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/period_intentions.md)

## Description

kit: in bob-ledger-tools, extract the shared property-card kit with no visible change: owned-key property hiding (generalized from the record sheet's observer), a `==` registry replacing the closed album|bank|record list, the host mount lifecycle, and shared `.bob-property-card` chrome. Move all three cards onto it. Align plugin docs so "card" means the panel and "card editor" means what `==` opens.

## Notes

[2026-11-19T23:10:53Z · bob-cli-nh.6.1.land] Phase closeout handoff for bob-cli-nh.7 (parent auto-closed by delegation when epic bob-cli-nh.6.1 closed; epic-symbols clean on both; no symvision recipe in justfile). Verified shared ownership (per-adapter path-tagged slots, generation-bound handles), instance-owned registry (builtins bank to album to record, extensions after; throwing matchers fail open), shared host lifecycle (Reading + Live Preview, path-bound failure removal/release, recovery on refresh), and chrome parity (24/24 exact vs 36d4801, .bob-property-card plus species classes). Acceptance on the repaired tree: album 120/121 (ctrl-j, bob-cli-nq), record 144/144, bank 73/78 (invalid-fence/walk-learn x2 baseline m6/m7; queue-card-live/reading pair is intervening-queue drift proven identical with repairs stashed, zero repair delta), bank setup 46/47 (ctrl-k nr) plus known arrange-save timeout (ns). Deployed 1.140.0 via bob plugins sync (main.js dd856af6da73600b, styles 9741733455cc7e2a match vault). Evidence: file:explicit:14696680ebb0a23080ad9414 and file:explicit:e5c34f58f439dc2d795d5d93. Extension contract for nh.7: registerPropertyCard({kind, match, open}) then a createPropertyCardHost adapter; no gate or host edits needed. Parent DECISIONS honored: day_summary_cap=sixty, authorized glossary strands only in their own phase, no declined decision-record writes. bob-cli-nh and period_intentions stay open for their lander.

## Dependencies

- **Blocks:** [bob-cli-nh.7](bob-cli-nh.7.md) ✓ · ⧖ 2026-11-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-nh.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nh.6.md) | [bob-cli-nh.6](bob-cli-nh.6.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-nh.6.1.3--3][1] | Verify only the requested phase closed and ancestors remain open | 1 |
| read-by | [agent:bob-cli-nh.6.1.land--1][2] | Need parent phase status before closeout | 1 |
| read-by | [agent:bob-cli-nh.land][3] | Need the child scope and notes | 1 |
| read-by | [agent:research.5i.cld][4] | Check property-card kit and intention card phase status for design research | 1 |
| read-by | [agent:research.5i.gem][5] | Verify ms and nh epic scope and decisions for research critique | 2 |
| read-by | [agent:research.5i.mus][6] | Need property-card kit phase scope for unification research | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nh.6.1.3.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nh.6.1.land.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nh.land.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.5i.cld/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.5i.gem/README.md
[6]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.5i.mus/README.md

<!-- sase:referenced-by:end -->
