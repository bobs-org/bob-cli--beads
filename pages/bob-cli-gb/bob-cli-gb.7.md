# Bead: bob-cli-gb.7 — bob-plugins: Event Task clock marks for #off, #on, and inherited rows, and the daily deprecation Notice

[Bead Pages](../README.md) / [bob-cli-gb](README.md) / bob-cli-gb.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.31.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.31.linker.w0.md) · **Assignee:** `bob-cli-gb.7` · **Size:** medium
**Created:** 2026-11-02 17:38:45 EST · **Closed:** 2026-11-03 00:02:25 EST
**Plan:** [202611/off\_on\_tags\_and\_offclock\_areas.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/off_on_tags_and_offclock_areas.md)

## Description

plugins-marks-notice: paint inherited off-clock Event Tasks dashed with a from-note tooltip, keep #off tag marks, give #on a neutral override tooltip in both views, and raise one Notice a day from deprecations[].

## Notes

[2026-11-03T05:02:02Z · bob-cli-gb.7] PROPOSED FOLLOW-UP: bob-plugins npm test 6 failures identical on clean master — Chromium missing in test-command-mode-sheet-sequence-dom.cjs (bob-cli-f1); freshness reload event [] vs obsidian-tasks-plugin:reload-open-search-results in test-ledger-tools-freshness-namespace.cjs (bob-cli-et); startup storm 1!==2 in test-ledger-tools-note-ready.cjs and relation scan timeout in test-ledger-tools-relation-index.cjs (bob-cli-eh); future Pending expected Blocked got Pending in test-navigation-hotkeys-schedule-work-log.cjs (bob-cli-ff); reduced-motion Chromium null!==0 in test-task-link-marks-motion.cjs (bob-cli-fz)

[2026-11-03T05:02:25Z · bob-cli-gb.7] Verified Live Preview and Reading paint inherited off-clock Event Tasks with a dashed pill and Off-clock · from {stem} tooltip (no tag chip), explicit #off/aliases keep the dashed pill plus tag chip, and #on paints a solid pill with On the clock (override). Deprecation Notice from deprecations[] fires once per day. 71 gcal-events + meet-event-run tests pass; npm run build:check, validate, and docs:check pass. Full npm test 6 failures match clean master (PROPOSED FOLLOW-UP cites bob-cli-f1, bob-cli-et, bob-cli-eh, bob-cli-ff, bob-cli-fz). bob plugins sync deployed bob-ledger-tools main.js; epic-symbols none leftover.

## Dependencies

- **Depends on:** [bob-cli-gb.4](bob-cli-gb.4.md) ✓ · ⧖ 2026-11-02
- **Depends on:** [bob-cli-gb.6](bob-cli-gb.6.md) ✓ · ⧖ 2026-11-02
- **Blocks:** [bob-cli-gb.8](bob-cli-gb.8.md) ✓ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-gb.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-gb.7/README.md) | [bob-cli-gb.7](bob-cli-gb.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@9185779`](https://github.com/bobs-org/bob-plugins/commit/9185779a99250a7a0c3033426efc38238086a5ed) | feat(gcal-events): paint inherited clock marks and daily deprecation Notice | [bob-cli-gb.7](bob-cli-gb.7.md) | 2026-11-03 00:04:14 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-gb.7][1] | Need the phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-gb.7/README.md

<!-- sase:referenced-by:end -->
