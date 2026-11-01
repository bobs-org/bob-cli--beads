# Bead: bob-cli-fb.3 — Obsidian picker and notice presentation

[Bead Pages](../README.md) / [bob-cli-fb](README.md) / bob-cli-fb.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bz](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bz.md) · **Assignee:** `bob-cli-fb.3` · **Size:** medium
**Created:** 2026-11-01 12:29:36 EST · **Closed:** 2026-11-01 13:12:48 EST
**Plan:** [202611/leaf\_project\_keep\_moving\_offers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/leaf_project_keep_moving_offers.md)

## Description

nav: teach bob-navigation-hotkeys' successor picker (v2) and Unblocked card (notice v2) to render keep_moving groups, captions, folds, and lane names.

## Notes

[2026-11-01T18:12:25Z · bob-cli-fb.3] PROPOSED FOLLOW-UP: 6 bob-plugins tests fail identically on the clean base (verified via git stash) — test-command-mode-sheet-sequence-dom (production sheet render), test-ledger-tools-freshness-namespace (create listener), test-ledger-tools-gcal-events (reload event), test-ledger-tools-note-ready (startup storm is linear), test-ledger-tools-relation-index (layout-ready scan), test-task-link-marks-motion (reduced-motion CSS, ~90s timeout); unrelated to nav picker/notice v2

[2026-11-01T18:12:48Z · bob-cli-fb.3] Nav v2 implemented in bob-plugins (bob-navigation-hotkeys 2.65.0): api.successors v2 (keep_moving group, caption, tag, folded blocked/scheduled, row lane names, derived title, skip-forward icon, one-line fold) and api.notice v2 (keep_moving rows, ⏭ card/title/fallback text, keeps ‹N› moving chip in mixed cards, silence when nothing picked); CSS uses only the Next token; new 703 exports fragment (700 is at the 1000-line cap); walk-toast composition test added. Verified: npm run build:check, docs:check pass; npm test 4750 pass / 6 fail where the same 6 fail on the clean base (recorded as PROPOSED FOLLOW-UP). bob plugins sync run for bob-navigation-hotkeys only (bob-ledger-tools skipped: another checkout holds an uncommitted deploy). Live Obsidian verification is left for Bryan.

## Dependencies

- **Depends on:** [bob-cli-fb.1](bob-cli-fb.1.md) ✓ · ⧖ 2026-11-01
- **Blocks:** [bob-cli-fb.4](bob-cli-fb.4.md) ◐ · ⧖ 2026-11-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-fb.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fb.3/README.md) | [bob-cli-fb.3](bob-cli-fb.3.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-fb.3][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fb.3/README.md

<!-- sase:referenced-by:end -->
