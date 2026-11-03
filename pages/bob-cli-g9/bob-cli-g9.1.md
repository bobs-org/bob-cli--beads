# Bead: bob-cli-g9.1 — Decay card hotfix and interim config

[Bead Pages](../README.md) / [bob-cli-g9](README.md) / bob-cli-g9.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.32.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.32.linker.w0.md) · **Assignee:** `bob-cli-g9.1` · **Size:** small
**Created:** 2026-11-02 15:55:42 EST · **Closed:** 2026-11-02 16:19:55 EST
**Plan:** [202611/task\_decay\_ladder.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_decay_ladder.md)

## Description

card-hotfix: make today's Ready decay card load the priority ladder (never this.config), enter P1 via a >= entry rule, put Enter and the focus ring on the same recommended row, give distinct config error copy, add a no-injection regression test, and set the interim chezmoi config (keeps 2, enter P1, rolls 2).

## Notes

[2026-11-02T21:19:36Z · bob-cli-g9.1] PROPOSED FOLLOW-UP: plugin npm test 7 failures on this tree match known environment/date flakes (wikilink index 12.2ms vs 12ms; Chromium missing command-mode sheet DOM and reduced-motion CSS; ledger-tools freshness-namespace reload-event withMissingConfig; note-ready startup storm 1 vs 2 scans and relationIndex layout-ready — bob-cli-eh; schedule-work-log expected Blocked got Pending for scheduled:: 2026-11-02 while today is 2026-11-02 — bob-cli-ff). Targeted decay-card tests 98/98; do not keep this phase open.

[2026-11-02T21:19:55Z · bob-cli-g9.1] Ready decay card loads the priority ladder via loadFreshnessDecayPrioritySnapshot (never this.config), with distinct missing/unreadable/invalid/no-property errors; P0 entry uses minDays >= interval so Bryan interval 3 / P1 min 3 enters P1; Enter and the focus ring share the recommended row; no plugin.config injection; chezmoi freshness.decay keeps 2 / enter P1 and priority.decay.rolls 2. Verified: plugin npm run build + docs:gen/docs:check, targeted decay-card tests 98/98, bob-cli just docs-check (447 passed), vault bob-navigation-hotkeys 2.71.0 via bob plugins sync --no-pull -F from this checkout (stale bob-cli_21 protection). Full npm test 5168/5175 with 7 pre-existing env/date flakes recorded as PROPOSED FOLLOW-UP.

## Dependencies

- **Blocks:** [bob-cli-g9.4](bob-cli-g9.4.md) ✓ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-g9.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-g9.1/README.md) | [bob-cli-g9.1](bob-cli-g9.1.md) | 3 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0f8ee84`](https://github.com/bobs-org/bob-cli/commit/0f8ee840f66d53db71fed9b864862f67c44245ca) | docs(freshness): enter P0 at the first level whose min\_days meets the interval | [bob-cli-g9.1](bob-cli-g9.1.md) | 2026-11-02 16:21:20 EST |
| bob-plugins | [`bob-plugins@a541b9c`](https://github.com/bobs-org/bob-plugins/commit/a541b9cc08ce9e76cd42beb5f0ad73ac646dca5c) | fix(nav): load the Ready decay card from the priority ladder | [bob-cli-g9.1](bob-cli-g9.1.md) | 2026-11-02 16:21:52 EST |
| chezmoi | [`chezmoi@44262a0`](https://github.com/bbugyi200/dotfiles/commit/44262a00df9b1a2c6d9b60d88362a486fb2d7ac2) | feat(bob): set interim decay keeps 2, enter P1, and two rolls | [bob-cli-g9.1](bob-cli-g9.1.md) | 2026-11-02 16:22:48 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-g9.1][1] | Need the phase scope, notes, and remaining close work | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-g9.1/README.md

<!-- sase:referenced-by:end -->
