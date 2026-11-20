# Bead: bob-cli-nu.4.1 — Complete inline command chips in Live Preview and Reading view

[Bead Pages](../README.md) / [bob-cli-nu.4](bob-cli-nu.4.md) / bob-cli-nu.4.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-nu.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-nu.4.md) · **Assignee:** `bob-cli-nu.4.1.land`
**Created:** 2026-11-20 07:37:00 EST · **Closed:** 2026-11-20 10:59:35 EST
**Plan:** [202611/command\_chips\_inline.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/command_chips_inline.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/command_chips_inline.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 6 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/command_chips_inline.md

<!-- sase:links:end -->

## Description

Finish bob-cli-nu.4 with safe source-aware activation, persistent live feedback, both inline renderers, and verified visual and Obsidian evidence.

## Notes

[2026-11-20T15:59:35Z · bob-cli-nu.4.1.land] Land verification (bob-plugins HEAD b52dd3f; bob-cli 1c5fd0fc). STEP 1: all five phases closed; every note addressed. Commits 52b7c31 (engine contract, Command Mode 0.4.0), e902351 (runtime, Bob Chips 0.8.0), fa28ece (Live Preview, 0.9.0), f381abc (Reading, 0.10.0), b52dd3f (preview, stub-bob e2e, print fix, 0.11.0). Read the source and it matches the plan contracts: 067 policy (no-run roots mail/ref/ref_history/.bob/_conflicts case-insensitive; absolute, drive-letter, backslash, and ./.. paths refused as unknown; query origin needs sourceVerified; engine looked up fresh), 075 activate (copy-only never reaches runText/openText; sync latch before the first await; post-await policy, source, and resolve recheck; only {source,onState} passed; Alt inert; no task/walk calls), 068 store (400 ms latch, 1.6 s completed), 061 Reading provenance (Tasks .task-description and Dataview task/list li verified; other query output is 'source note unknown'; embed src mismatch is unknown; no MutationObserver), no innerHTML/dataset payloads. Parent inline-phase items 1-7 are all present; docs/bob-chips.md does not claim fence/keymap/author as shipped. Shared hooks for nu.5/nu.6 are exported (store armed target, commandChipActivate, mount, paint, eligibility; plugin.commandChipRunHotkey). Hand-edited fragments are all <=977 lines. Reran: npm run validate 12/12; chip, Command Mode contract, and e2e self-test suites 204/204; copy-chip Live Preview perf 5/5 (mixed 2,000-line case); BOB_CLI_DIR=this bob-cli npm run docs:check passes every gate, so the earlier baseline URL failure (fixed by 3956368) and the glossary drift (fixed in bob-cli 1c5fd0fc) are both gone. Real-Obsidian e2e on athena: 23/23 per acceptance artifact file:explicit:bba2a234f264129a97f260c8. bob plugins list: bob-chips 0.11.0 and bob-command-mode 0.4.0 synced and enabled; sync without force. STEP 2: post-start commits (bob-plugins 5c41b5b, e643931, 3956368; bob-cli ab341446, b7007011, 46bb654a, 1c5fd0fc) touch ledger-tools, nav pickers, capture, periods, and install. None overlaps or should consume command chips (GTD adoption belongs to the later adopt phase), so no integration edits were needed. FOLLOW-UP TRIAGE: (a) baseline failures (4.1.1#1, .2#2, .3#2, .4#2, .5#2): ledger 25 ms perf asserts are already tracked by bob-cli-km/bob-cli-io, so no new task; the URL gate bob-cli-nv now passes (noted on bob-cli-nv). (b) 4.1.1#2 preview-first report rows refuse Ctrl+Enter and chip runs: created bob-cli-o5 (bug, small, ready). (c) plugin-apis.md word budget, 7,980/8,000 (4.1.2#3, .3#3, .4#3): recorded as a DISCOVERED ISSUE on active parent epic bob-cli-nu, plus a heads-up on bob-cli-nu.6, whose keymap docs will cross the cap. Not split here because a page split is an IA move that needs an approved plan and preserved URLs, and the page is still within budget. (d) 4.1.5#1 bob-cli glossary drift: declined, already fixed at bob-cli 1c5fd0fc. (e) 4.1.4#4 Dataview inline-field values copy-only: declined; this is the plan's conservative unknown-copies contract, and there is no observed demand. (f) 4.1.5#3 Reading-view long-chip wrap shape (button lays out inline-block): declined; it is the plan's required real-button tradeoff, shared with existing copy chips, and text stays untruncated. epic-symbols: none for nu.4.1 or nu.4. Reload Obsidian for the 0.11.0 CSS print fix.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-nu.4.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.4.1.land/README.md) | [bob-cli-nu.4.1](bob-cli-nu.4.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-nu.4.1.1][1] | Need epic decisions and context | 1 |
| read-by | [agent:bob-cli-nu.4.1.2][2] | Need epic decisions | 1 |
| read-by | [agent:bob-cli-nu.4.1.3][3] | Need epic decisions and notes | 1 |
| read-by | [agent:bob-cli-nu.4.1.4][4] | Need epic decisions | 1 |
| read-by | [agent:bob-cli-nu.4.1.5][5] | Need epic decisions and context for phase 5 | 1 |
| read-by | [agent:bob-cli-nu.4.1.land][6] | Need the epic scope, children, and linked plan file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.4.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.4.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.4.1.3/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.4.1.4/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.4.1.5/README.md
[6]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.4.1.land/README.md

<!-- sase:referenced-by:end -->
