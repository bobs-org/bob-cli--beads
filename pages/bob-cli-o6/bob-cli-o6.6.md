# Bead: bob-cli-o6.6 — Real-Obsidian proof, preview matrix, live album tidy, and final deploy

[Bead Pages](../README.md) / [bob-cli-o6](README.md) / bob-cli-o6.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1eh](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1eh.md) · **Assignee:** `bob-cli-o6.6` · **Size:** large
**Created:** 2026-11-20 11:49:17 EST · **Closed:** 2026-11-21 15:06:05 EST
**Plan:** [202611/property\_card\_title\_block.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/property_card_title_block.md)

## Description

obsidian-proof: add and run a real-Obsidian title-block walkthrough on athena (ownership, reveal, fallback, heading links, Outline, byte neutrality, grayscale, forced colors), render the full preview matrix, fix what it finds, run the live bob albums tidy only when every host runs a bob that reads album `title:`, pass every gate, and deploy the final tree.

## Notes

[2026-11-21T20:06:55Z · bob-cli-o6.6.1.land] Delegated closeout verified by the bob-cli-o6.6.1 land agent. Every obsidian-proof item landed. (1) Real-Obsidian title-block walkthrough on athena covers ownership, reveal, fallback/teardown, heading links, Outline, and byte neutrality: 65/65, rerun on bob-plugins e6d7aed. (2) Full preview matrix with grayscale and forced colors: 77/77 captures, all inspected. (3) Recovery defect it found was fixed in 238fa91. (4) Live bob albums tidy ran only after athena, apollo, and mac all proved title-first reads: vault commit 3f9861acf863, idempotent. (5) Gates: build:check, npm test 8246/0, and just check pass. The docs gates fail only on other epics' pages (nav-hotkeys page from bob-cli-om, ledger-tools page from bob-cli-oo, test_contracts from bob-cli-on), all routed. (6) Final tree deployed through guarded sync, no -F. For the outer land agent: evidence manifest file:explicit:6a34814f8b6f320845a11587, rerun evidence file:explicit:a32022c60d3fc54dd426ac59. The full follow-up triage is in the bob-cli-o6.6.1 close note: new bob-cli-or; +1 on io, km, il; DISCOVERED ISSUE on bob-cli-on and bob-cli-oo; bob-cli-oq closed as fixed; bob-cli-oc repaired by cb9f8fad and left open for you.

## Dependencies

- **Depends on:** [bob-cli-o6.3](bob-cli-o6.3.md) ✓ · ⧖ 2026-11-20
- **Depends on:** [bob-cli-o6.4](bob-cli-o6.4.md) ✓ · ⧖ 2026-11-20
- **Depends on:** [bob-cli-o6.5](bob-cli-o6.5.md) ✓ · ⧖ 2026-11-20
- **Blocks:** [bob-cli-o6.7](bob-cli-o6.7.md) ✓ · ⧖ 2026-11-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-o6.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-o6.6.md) | [bob-cli-o6.6](bob-cli-o6.6.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-o6.6.1.1][1] | Need parent DECISIONS, notes, and whether earlier title-walkthrough work already landed | 1 |
| read-by | [agent:bob-cli-o6.6.1.3][2] | Need parent epic scope and decisions | 1 |
| read-by | [agent:bob-cli-o6.6.1.land][3] | Verify the delegated phase scope is covered by the closed child epic | 1 |
| read-by | [agent:bob-cli-o6.7][4] | Check final proof notes for shipped-behavior deviations before writing glossary strands | 1 |
| read-by | [agent:bob-cli-oj.5.1.1][5] | Check open o6 phases for fragment coordination before editing 240g/styles.css | 1 |
| read-by | [agent:bob-cli-oj.5.1.2][6] | Coordination precondition: which o6 phases are open and which fragments they touch | 1 |
| read-by | [agent:bob-cli-oj.5.1.3][7] | bob-cli-o6 precondition: check open phases editing fragments I will touch | 1 |
| read-by | [agent:bob-cli-oj.5.1.4][8] | Coordination precondition: which o6 phases are open and which fragments they touch | 1 |
| read-by | [agent:bob-cli-oj.6][9] | Need o6.6 description to confirm it does not edit footer fragments 120/121/124 | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-o6.6.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-o6.6.1.3/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-o6.6.1.land/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-o6.7/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.1/README.md
[6]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.2/README.md
[7]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.3/README.md
[8]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.4/README.md
[9]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.6/README.md

<!-- sase:referenced-by:end -->
