# Bead: bob-cli-7c.5 — Navigation hotkeys successor picker modal and walk integration

[Bead Pages](../README.md) / [bob-cli-7c](README.md) / bob-cli-7c.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.11.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.11.linker.w0.md) · **Assignee:** `bob-cli-7c.5` · **Size:** large
**Created:** 2026-10-13 09:48:12 EDT · **Closed:** 2026-10-13 11:29:53 EDT
**Plan:** [202610/successor\_offers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/successor_offers.md)

## Description

nav_picker: add the api.successors v1 multi-select picker (groups, muted rows, filter, Tab/Ctrl+A marks, double-press guard, plan meter), hold the review-walk gesture through the picker so the walk advances once after it settles, and update the unblocked notice copy.

## Notes

[2026-10-13T15:29:42Z · bob-cli-7c.5--1] Verified: focused picker suite 125/125 pass (successor-picker, review-advance, review-advance-gestures, checklist-ctrl-enter, unblocked-notice, picker-lifecycle) after rebuild; npm run validate passes; git diff --check clean. Full npm test: 2678 pass, 6 fail — 5 pre-existing on clean base (4x test-ledger-tools-unblocked-glyph, Keep-counts in test-navigation-decision-card-handlers, reproduced via stash on base commit) + 1 flaky perf gate (stage-entry 1000-task 16ms budget: 30ms under full-suite load, 10/10 pass in isolation on this tree). just check: 1465 pass, 2 fail in capture ref percent_listen audio-worker tests (ENOENT listen invocation, bob-cli tree clean so base-identical, unrelated to nav JS). bob plugins sync --no-pull succeeded; --dry-run shows no drift (0 to copy, 3 unchanged).

[2026-10-13T15:29:53Z · bob-cli-7c.5--1] nav_picker done: successor picker modal (206-successor-picker-modal.js), api.successors v1, review-walk hold, notice copy; focused 125/125, validate ok, diff-check clean, sync+no-drift verified; full-suite failures proven pre-existing/flaky on base

## Dependencies

- **Depends on:** [bob-cli-7c.1](bob-cli-7c.1.md) ✓ · ⧖ 2026-10-13
- **Blocks:** [bob-cli-7c.6](bob-cli-7c.6.md) ✓ · ⧖ 2026-10-13
- **Blocks:** [bob-cli-7c.8](bob-cli-7c.8.md) ◐ · ⧖ 2026-10-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-7c.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-7c.5.md) | [bob-cli-7c.5](bob-cli-7c.5.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-7c.5--1][1] | implement approved successor picker plan; review monitor failures | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-7c.5.md

<!-- sase:referenced-by:end -->
