# Bead: bob-cli-99.3 — The bob-reading-board block, interaction, and look

[Bead Pages](../README.md) / [bob-cli-99](README.md) / bob-cli-99.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.8z](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.8z.md) · **Assignee:** `bob-cli-99.3` · **Size:** medium
**Created:** 2026-10-18 13:02:21 EDT · **Closed:** 2026-10-18 15:22:28 EDT
**Plan:** [202610/reading\_board.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/reading_board.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:0d26553ff3f1016f4f1ed96f | attached via sase artifact create --bead |
| related | file:explicit:164f9489dab97761ea83b90b | attached via sase artifact create --bead |
| related | file:explicit:17c8788833a8dbef0b37ee3c | attached via sase artifact create --bead |
| related | file:explicit:2f2c5f0e008255e54d86ca86 | attached via sase artifact create --bead |
| related | file:explicit:3475cef66268a722d957bb90 | attached via sase artifact create --bead |
| related | file:explicit:381e7da3a98172e94d4df4f3 | attached via sase artifact create --bead |
| related | file:explicit:38da2a02a792bdae1ef0a59c | attached via sase artifact create --bead |
| related | file:explicit:3b8bcb760cd3a1f888ac1490 | attached via sase artifact create --bead |
| related | file:explicit:6fc04c1d68623c413edc873b | attached via sase artifact create --bead |
| related | file:explicit:75b5c5d4877dd29a4124b4d5 | attached via sase artifact create --bead |
| related | file:explicit:9fd447a5a05e2cb453d012a4 | attached via sase artifact create --bead |
| related | file:explicit:b2af40a8bbd78ec86a317a92 | attached via sase artifact create --bead |
| related | file:explicit:cf7f225a62d4936e91e20d82 | attached via sase artifact create --bead |
| related | file:explicit:d4cbe67b8a478a5970be5165 | attached via sase artifact create --bead |
| related | file:explicit:eac7f077d746360050eb8e75 | attached via sase artifact create --bead |
| related | file:explicit:eef322a5aef43cd0beacf98a | attached via sase artifact create --bead |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

board-ui: render the board (lanes, cards, Snoozed rows, honest states), keyboard and mouse routing, the Open Reading Board command, the optional Highlights hand-off, CSS, and a screenshot preview harness reviewed in both themes and three widths.

## Notes

[2026-10-18T19:22:13Z · bob-cli-99.3] PROPOSED FOLLOW-UP: Record decisions:reading-board-is-bob-rendered — skipped here because the epic auto-decided memory_board_record=no; claim: the board is a bob-reading-board block drawn from bob ref list JSON, read-only, blocked refs in a Snoozed lane with blocked_by reasons; rejected: a Bases kanban grouped by frontmatter status (it cannot see the ^ref task) and a JS mirror of the blocking rules; cost: a spawn per revalidation; reopens when Bases can read task lines or the spawn fails on the Mac; run sase memory init after.

[2026-10-18T19:22:28Z · bob-cli-99.3] Added the bob-reading-board block in bob-ledger-tools (fragments 243 render builders, 244 block/interaction, styles.css section) plus nav openReferencePdf (pdf_action=yes). Verified: new fake-DOM suite test-ledger-tools-reading-board-block.cjs (24 tests) and nav api tests pass; npm test = 3077 pass, 7 fail identical to the clean-base failures already recorded on bob-cli-99.2 (bob-cli-6v/6w/3w/7i); build:check and validate clean; bob plugins sync --repo deployed both plugins. Preview harness scripts/preview-reading-board.cjs runs 91 real-Chromium checks (3 widths x 2 themes, hover, touch, forced colors, keys/mouse routing, contrast >= 4.5, every honest state) with 16 screenshots reviewed and attached to this bead; live bob ref list JSON (46 refs) renders 2/5/16/23 lanes matching the JSON. just all not rerun: bob-cli repo unchanged this phase. Skipped memory decision recorded as PROPOSED FOLLOW-UP.

## Dependencies

- **Depends on:** [bob-cli-99.2](bob-cli-99.2.md) ✓ · ⧖ 2026-10-18
- **Blocks:** [bob-cli-99.4](bob-cli-99.4.md) ✓ · ⧖ 2026-10-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-99.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-99.3/README.md) | [bob-cli-99.3](bob-cli-99.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@74e3d9b`](https://github.com/bobs-org/bob-plugins/commit/74e3d9bcfc913e3964c058319effc3e976e2239a) | feat(reading-board): add the bob-reading-board block, keyboard and mouse routing, and Highlights hand-off | [bob-cli-99.3](bob-cli-99.3.md) | 2026-10-18 15:23:22 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-99.3][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-99.4][2] | Need what board-ui delivered | 1 |
| read-by | [agent:bob-cli-99.land--2][3] | Reread child scope and all completion/triage notes before closing the Reading Board epic | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-99.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-99.4/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-99.land.md

<!-- sase:referenced-by:end -->
