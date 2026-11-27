# Bead: bob-cli-rc.3 — Jump integration, lifecycle controller, landing flash, and peek

[Bead Pages](../README.md) / [bob-cli-rc](README.md) / bob-cli-rc.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1hg](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1hg.md) · **Assignee:** `bob-cli-rc.3` · **Size:** medium
**Created:** 2026-11-27 15:06:05 EST · **Closed:** 2026-11-27 16:44:47 EST
**Plan:** [202611/ctrl\_jk\_section\_map.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/ctrl_jk_section_map.md)

## Description

wiring: move the section jump into a new fragment, fix the double scroll, add the landing flash, the hold/linger/fade lifecycle with activity dismissal, the doc-keyed heading cache, the aria-live sentence, and the unbound peek command.

## Notes

[2026-11-27T21:44:30Z · bob-cli-rc.3] PROPOSED FOLLOW-UP: test-snooze-model-vectors "snooze-add-resnooze-replaces-history daily postimage" still fails identically on clean bob-plugins master — already owned by bob-cli-q5; wiring did not change it.

[2026-11-27T21:44:47Z · bob-cli-rc.3] Wiring landed in bob-plugins navigation 2.107.16: 611 lifecycle (hold/linger/pinned/fade, generation-guarded timers), 612 controller (ctx host resolve, WeakMap heading cache, activity dismissal, rAF paint, 400ms aria-live), 613 jump/peek (jump first/map second, no double scroll, wrapped, mobile skip). Jump removed from 610; ctx + unbound show-section-map registered; landing flash generalized to flashEditorLandingLine. Peek is pinned. Gate: npm run build, build:check, docs:gen, docs:inventory:check pass; focused lifecycle/jump/section-nav 31/31. Full npm test 10402 pass / 1 fail / 4 skipped — the fail is snooze-add-resnooze-replaces-history, identical on clean master and owned by bob-cli-q5. bob plugins sync copied the plugin. No --epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-rc.1](bob-cli-rc.1.md) ✓ · ⧖ 2026-11-27
- **Depends on:** [bob-cli-rc.2](bob-cli-rc.2.md) ✓ · ⧖ 2026-11-27
- **Blocks:** [bob-cli-rc.4](bob-cli-rc.4.md) ✓ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-rc.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-rc.3/README.md) | [bob-cli-rc.3](bob-cli-rc.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@592c3c9`](https://github.com/bobs-org/bob-plugins/commit/592c3c9afbad50b95af1bda7029158da15923931) | feat(navigation): wire Section Map lifecycle, jump, and pinned peek | [bob-cli-rc.3](bob-cli-rc.3.md) | 2026-11-27 16:53:20 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-rc.3][1] | Need the phase scope, notes, design file, and DECISIONS before closing | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-rc.3/README.md

<!-- sase:referenced-by:end -->
