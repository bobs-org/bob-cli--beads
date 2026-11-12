# Bead: bob-cli-kd.6.1 — Bank views and safe editing in Obsidian

[Bead Pages](../README.md) / [bob-cli-kd.6](bob-cli-kd.6.md) / bob-cli-kd.6.1

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-kd.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kd.6.md) · **Assignee:** `bob-cli-kd.6.1.land`
**Created:** 2026-11-11 14:27:33 EST
**Plan:** [202611/bank\_obsidian.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_obsidian.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/bank_obsidian.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 8 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_obsidian.md

<!-- sase:links:end -->

## Description

Finish bob-cli-kd.6 with month and queue cards, a daily chip, safe bank-row editing, styled rows in both Obsidian views, and verified plugin deployment.

## Notes

[2026-11-12T13:09:54Z · bob-cli-kd.6.1.land] LANDING TRIAGE (kd.6.1.land) of every child PROPOSED FOLLOW-UP: (1) 6.1.1 #1 bob plugins sync literal-pathspecs failure: declined, already fixed (bob-cli 1a9b6828; sync works from this host). (2) 6.1.2 #1 docs:check word budgets: declined, resolved; the epic's own d2e4137 later pushed bob-ledger-tools.md to 6012/6000 after rebasing on albums bd6fc41, which the lander fixed by trimming the bank section (lint ok); headroom context added to bob-cli-il. (3) 6.1.2 #2 load-sensitive timing tests: reduced-motion +1 on bob-cli-fz, keep-moving +1 on bob-cli-ki; wikilink CPU budgets declined, addressed by d94c6bb (serial perf stage) after the note. (4) 6.1.3 #2 rollout smoke command: declined, fixed in 564f3c1 deployment.md. (5) 6.1.3 #4/#5 and 6.1.5 #4 picker runtime test never exits: new task bob-cli-ks (pre-existing on 99ccca1). (6) 6.1.3 #6, 6.1.4 #1, 6.1.5 #3 strict Zensical missing vim-yank-flash page: DISCOVERED ISSUE corroboration on active epic bob-cli-kb, no task. (7) 6.1.5 #2 day-strip-plan-host test never exits: declined as follow-up; it is EPIC-CAUSED (bisected to 4e4a580: 241p 60 s config interval used a globalThis fallback without the timer-host guard), fixed by the lander; test 19/19 exits in 3 s. (8) 6.1.5 #5 final sync after the album author: done, ledger-tools 1.112.1 deployed without -F via the documented clean-then-descendant sync.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kd.6.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.6.1.land/README.md) | [bob-cli-kd.6.1](bob-cli-kd.6.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@a6f4b03`](https://github.com/bobs-org/bob-plugins/commit/a6f4b035a653489331134bf326788de8e654da10) | fix(ledger-tools): guard bank marks config timer and trim bank docs under cap | [bob-cli-kd.6.1](bob-cli-kd.6.1.md) | 2026-11-12 08:12:49 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kd.6.1.1][1] | Need epic DECISIONS and bank-ui-data phase scope | 1 |
| read-by | [agent:bob-cli-kd.6.1.2][2] | need parent epic scope and decisions | 1 |
| read-by | [agent:bob-cli-kd.6.1.4][3] | Need parent epic DECISIONS for bank-ui-marks | 1 |
| read-by | [agent:bob-cli-kd.6.1.5][4] | Need child epic scope and sibling phase status | 1 |
| read-by | [agent:research.49.cld][5] | research: user guide for first-time bank ack and e2e test of bob-cli-kd | 1 |
| read-by | [agent:research.49.final][6] | Check sub-phase state and any notes for the consolidated kd e2e test gating | 1 |
| read-by | [agent:research.49.gem][7] | Check phase 6.1 sub-bead | 1 |
| read-by | [agent:research.49.mus][8] | kd obsidian child epic status for guide | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.6.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.6.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.6.1.4/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.6.1.5/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.49.cld/README.md
[6]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.49.final/README.md
[7]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.49.gem/README.md
[8]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.49.mus/README.md

<!-- sase:referenced-by:end -->
