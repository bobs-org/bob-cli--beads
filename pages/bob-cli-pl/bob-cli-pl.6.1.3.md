# Bead: bob-cli-pl.6.1.3 — Implement simple setting stages and clear-to-inherit through the shared session

[Bead Pages](../README.md) / [bob-cli-pl.6.1](bob-cli-pl.6.1.md) / bob-cli-pl.6.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pl.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pl.6.md) · **Assignee:** `bob-cli-pl.6.1.3` · **Size:** medium
**Created:** 2026-11-24 15:49:21 EST · **Closed:** 2026-11-25 06:13:16 EST
**Plan:** [202611/area\_project\_settings.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/area_project_settings.md)

## Description

setting-actions: add the five simple controls, temporary generic stages, typed set/clear operations, effects and warnings, and fresh contract reconciliation after apply and undo.

## Notes

[2026-11-25T11:12:38Z · bob-cli-pl.6.1.3] PROPOSED FOLLOW-UP: load-only timing failures, already tracked by bob-cli-km and bob-cli-pg — npm test under suite load failed only event-link-times 200-link 25 ms (91.1 ms) and frees-marks 200-link/2000-task 25 ms (150 ms); test:perf typed keystroke p95 14.8/12 ms. Both ledger-tools files passed in isolation on this tree (event-link-times build 5.6 ms) and on clean HEAD c1819664 (event-link-times 4.6 ms, frees-marks 23.0 ms, typed p95 10.98 ms). Unchanged from 6.1.2 note #2.

[2026-11-25T11:12:46Z · bob-cli-pl.6.1.3] PROPOSED FOLLOW-UP: docs-check baseline exceeds word budgets — BOB_CLI_DIR=this workspace reported plugin-apis.md 9,287/8,000, mac-capture/keyboard.md 6,019/6,000, mac-capture/protocol.md 6,308/6,000, bob-navigation-hotkeys.md 6,029/6,000. This phase only added a short architecture.md seam paragraph; those inputs match 6.1.2 notes #1/#2.

[2026-11-25T11:13:16Z · bob-cli-pl.6.1.3] Verified setting-actions in bob-plugins: fragments 298x/298y after 298w (259/535 lines; 298f stays 933). Summary is one-line with live N/140 (multiline refused, over-140 warns without blocking). Ready cap is 1–999 or off (legacy false→off; o toggles off; effect line uses local noteReady). Review is 1–365 with residence-only help. Capture names reuse the ordered list stage as setting.set. Stats-root Enter is one undoable set-true or clear, never root:false, locked on top-level projects. Temporary generic parent (prose)/color/type/clock stages; clock setting.set is always a {mode, types?} object. Ghost Enter seeds from effectiveValue and writes nothing. Dedicated saves use setting.set; Ctrl+D is setting.clear (ghost no-op, parent refused). Setting batches dry-run via setDraft+previewNow before apply. Confirmed post-apply/undo/redo contract is adopted; dry-run candidates never become the modal report; missing additive contract invalidates and re-reads props show. Resolver seam propertyEditorRegisterSettingStageHandler is documented in docs/develop/architecture.md. Tests: setting-actions 16/16, settings-rows 19/19, related property-editor 128/128. npm run build and build:check clean. bob plugins sync copied ledger-tools main.js (+821) and styles.css. epic-symbols: none. Load-only timing and docs word-budget baselines recorded as PROPOSED FOLLOW-UP (bob-cli-km / bob-cli-pg; 6.1.2 notes). No memory edits.

## Dependencies

- **Depends on:** [bob-cli-pl.6.1.2](bob-cli-pl.6.1.2.md) ✓ · ⧖ 2026-11-24
- **Blocks:** [bob-cli-pl.6.1.4](bob-cli-pl.6.1.4.md) ✓ · ⧖ 2026-11-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pl.6.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pl.6.1.3/README.md) | [bob-cli-pl.6.1.3](bob-cli-pl.6.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@e1a4d1c`](https://github.com/bobs-org/bob-plugins/commit/e1a4d1cff0dc1e77d2be07f19ac0b39862db88d6) | feat(props): add Property Editor setting stages and clear-to-inherit | [bob-cli-pl.6.1.3](bob-cli-pl.6.1.3.md) | 2026-11-25 06:15:10 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pl.6.1.3][1] | Need the phase scope, design file, notes, and epic DECISIONS | 6 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pl.6.1.3/README.md

<!-- sase:referenced-by:end -->
