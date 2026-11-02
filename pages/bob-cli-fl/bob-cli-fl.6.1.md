# Bead: bob-cli-fl.6.1 — Stats clocks and the Day strip off-clock hint

[Bead Pages](../README.md) / [bob-cli-fl.6](bob-cli-fl.6.md) / bob-cli-fl.6.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-fl.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-fl.6.md) · **Assignee:** `bob-cli-fl.6.1.land`
**Created:** 2026-11-02 05:03:38 EST · **Closed:** 2026-11-02 12:45:09 EST
**Plan:** [202611/stats\_clock\_ui.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/stats_clock_ui.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/stats_clock_ui.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/stats_clock_ui.md

<!-- sase:links:end -->

## Description

Complete bob-cli-fl.6 with a persistent Worked, Off-clock, and Total Stats control, accurate dashed clock renderings, and a Day strip link to the selected day's off-clock time while preserving Worked facts and lanes.

## Notes

[2026-11-02T17:09:52Z · bob-cli-fl.6.1.land] FOLLOW-UP TRIAGE (land agent): +1 bob-cli-ff (schedule-work-log future Pending; from fl.6.1.2/.3/.4/.5 #1); +1 bob-cli-f1 (command-mode-sheet-sequence-dom Chromium discovery; .3/.4/.5); +1 bob-cli-et (freshness-namespace reload; .2/.3/.4); +1 bob-cli-eh (note-ready startup scan count + relation-index replay; .2-.5); +1 bob-cli-ej (freshness Live Preview perf gate = .5 #1 'freshness keystroke perf'); +1 reopened bob-cli-e4 (vault nav-hotkeys/task-status-cycler stuck on bob-cli_21 dirty deploy @7dbbb6d; .5 #2). NEW bob-cli-fy (systemic: sync keeps refusing dirty agent deploys after their content lands; .5 #2 + land evidence). NEW bob-cli-fz (headless Chromium screenshots intermittently hang on apollo, harnesses lack CDP timeouts and orphan browsers; covers .5 #1 task-link-motion reduced-motion). NEW bob-cli-g0 (preview-day-strip 410px screenshot-day shows 2 roots; reproduced at 806ba69, 75e7875 and pre-epic 71ae1cb; from .5 close note). DECLINED as tasks: .5 #3 Stats preview hang — epic-caused (75e7875 JS deterministically wedges the 1000px full-page capture; 33318e0 passes in 14 s on the same host; JS4+CSS3 hangs, JS3+CSS4 passes), so it is landing-tale work; .5 #2 bob-ledger-tools sync refusal — epic deploy work for the landing tale (vault build = 3a2b03b minus concurrently landed 7a647e8, provably on master); .5 #1 unnamed 'one perf flake' — no identifying test name, nothing actionable beyond bob-cli-ej/bob-cli-f8.

[2026-11-02T17:45:09Z · bob-cli-fl.6.1.land] Landing verified. Phase commits: bob-cli 247440cc, 69c6458c; bob-plugins 3a2b03b, 33318e0, 75e7875, 806ba69. Tale fixes: (1) failed Off-clock/Total fetch falls back to Worked once via in-memory state.clock=worked, no stored-preference change, plus bounded regression test (1 render, <=2 fetches, preference unchanged); (2) 360px overflow fixed by statsClockWrapValue NBSP segments plus normal-wrap home-value/lane-meta CSS, matrix shows no overflow at 360/1000 light/dark; (3) preview-stats-block harness: Phase-4 lanes/panels wedge full-page compositor capture, switched to content-height viewport plus normal capture with per-call CDP timeouts and detached Chromium process-group kill, exits 0 with 30/30 interaction checks; clock off-clock/total/forced-colors screenshots written and inspected via matrix report; (4) docs: bob-plugins Day-strip hint and clock-control/marks/Total-overlap plus Stats-page link, bob-cli Obsidian dashed-meaning paragraph with Total sentence and empty-state, clock-aware window-bars meta/title/sentences/windowKey/forced-colors with Day-strip unchanged. Tests: focused stats+day-strip suites 290 pass; npm test 5132 pass / 5 fail, all 5 match tracked knowns (schedule-work-log ff, sheet-sequence-dom f1, freshness-namespace et, note-ready + relation-index eh); npm run build:check ok; npm run validate 8/8 ok; BOB_CLI_DIR docs:check ok; preview-day-strip 264 cells with only the 4 known 410px screenshot-day failures (g0); just check ok; just docs-check ok. Browsers: headless Chromium matrix ran (360/1000 light/dark + clock lenses + forced-colors); no browser scenario was skipped except the absent dataviz validator noted in the matrix report. Deploy: force_sync_ledger_tools=force; deploy json unchanged (bob-cli_14/3bab3c0, digest 6c146eaa, 2026-11-02T11:43Z), forced bob-ledger-tools 1.91.0 via sync -F with backup, confirm -n up to date; nav-hotkeys/task-status-cycler never forced (e4/fy). Triage: ff, f1, et, eh, ej, e4 corroborated; fy, fz, g0 filed. just symvision has no recipe in this checkout, epic-symbols clean for both beads.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-fl.6.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-fl.6.1.land.md) | [bob-cli-fl.6.1](bob-cli-fl.6.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`99fe1ce`](https://github.com/bobs-org/bob-cli/commit/99fe1ce49a73154a49ffb904e4856a99ce708c79) | docs(stats): finish clock user docs for Obsidian Stats block and window bars | [bob-cli-fl.6.1](bob-cli-fl.6.1.md) | 2026-11-02 12:47:44 EST |
| bob-plugins | [`bob-plugins@af97bcd`](https://github.com/bobs-org/bob-plugins/commit/af97bcde201293c567f005450d47585d16a92bda) | feat(ledger-tools): land Stats clock fixes, preview harness hardening, and clock docs | [bob-cli-fl.6.1](bob-cli-fl.6.1.md) | 2026-11-02 12:48:39 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-fl.6.1.2][1] | Need the approved parent design and final decisions for this phase | 1 |
| read-by | [agent:bob-cli-fl.6.1.3][2] | Need epic DECISIONS and phase scope | 2 |
| read-by | [agent:bob-cli-fl.6.1.4][3] | Need the epic decisions governing this phase | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fl.6.1.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fl.6.1.3/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fl.6.1.4/README.md

<!-- sase:referenced-by:end -->
