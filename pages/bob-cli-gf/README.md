# Bead: bob-cli-gf — Off-clock link chips — show the \`#off\` chip after ledger Task Links to off-clock tasks

[Bead Pages](../README.md) / bob-cli-gf

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.c9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.c9.md) · **Assignee:** `bob-cli-gf.land`
**Created:** 2026-11-03 09:51:50 EST
**Plan:** [202611/off\_clock\_link\_chips.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/off_clock_link_chips.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/off_clock_link_chips.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/off_clock_link_chips.md

<!-- sase:links:end -->

## Description

In a daily note's Pomodoro ledger, every Task Link whose task resolves off the clock (an explicit `#off` or alias, or an inherited area/project `offclock: true`) wears the same dashed `timer-off` `off` chip that off-clock Event Tasks already wear, in Live Preview and Reading view, so Bryan can see at a glance which planned or logged work will keep a session off the work clock.

## Notes

[2026-11-03T15:39:17Z · 17b--code] CROSS-EPIC COORDINATION with bob-cli-gg (Event link times). Not remaining work for any phase. Checklist for whichever of gf/gg commits to bob-plugins second, and for this land agent (confirm each item). gf's plan predates gg and has no coordination section; gg's plan has one, and these items add what both plans lack.

State when written (2026-11-03): gf.1 landed in bob-cli (5f35f0b3); gg.1 is closed; no gf or gg commit in bob-plugins yet (master 175aced, bob-ledger-tools 1.95.0); gf.2, gf.3, gg.2, and gg.3 remain in flight.

1. Same hunks; expect textual conflicts and resolve by keeping both features:
   - `src/269-plugin-progress-marks-reading.js` `ledgerMarkClass` list must hold BOTH `bob-off-clock-link-chip` and `bob-event-link-time`. Dropping either one makes rows wearing that host stop counting as ledger rows: ◐/🔓/🔑 vanish and a status ring appears.
   - `src/279-plugin-task-theme-api.js` `taskThemeRequestSourceText` fill callback: keep both refresh calls (`scheduleOffClockLinkChipsRefresh`, `scheduleEventLinkTimesRefresh`).
   - `styles.css` calendar block (about lines 5240-5370): gf adds `.bob-off-clock-link-chip` to the Event off-clock chip rules and renames `--bob-calendar-off-clock-icon` to a body-level `--bob-off-clock-icon`; gg appends its host rule after the wing rules, right next to that variable. Nothing may keep using the old variable name.
   - `src/350-exports.js` tail, the `package.json` "test" line, the `manifest.json` description, and `docs/bob-ledger-tools.md` ("Marks and rendered blocks", "Session toggles", "Calendar Events").
   - Separate spots that should auto-merge: `src/fragments.json`, `src/310-install-methods.js`.
2. Generated output: never hand-merge `main.js` or `npm run docs:gen` output. Resolve the `src/` and docs sources, then rerun `npm run build`, `npm run docs:gen`, and `npm run build:check`.
3. `manifest.json` version: both plans bump the minor from 1.95.0. The second to land takes the next minor past master at commit time (1.97.0 if the first took 1.96.0).
4. `bob plugins sync`: both epics' phase 2 and phase 3 run it. Its deploy guard refuses to overwrite another checkout's uncommitted or non-ancestor deploy, and the refusal text suggests `-F`. If the refusal names the other epic's checkout, do NOT use `-F`; that rolls the other feature out of Bryan's vault. Rebase onto a bob-plugins master that contains the other epic's commit, rebuild, and sync again. If that commit is not on master yet, record the sync as pending in a phase note.
5. Intended overlap, keep both: a ledger link to an off-clock Event Task wears gg's dashed time pill before the link and gf's `off` chip after it (`pill link 🔓 🔑 N off`). Neither epic should hide the other's mark.
6. Parity: both decide the clock with `taskEffectiveClockResolution` (gf through `pomodoroClockLinkFacts`, gg through `gcalEventsApplyClockToRow`). Once both have landed, a row's pill has `data-off-clock="true"` exactly when the row wears the chip. Known transient gap: a full-path same-note link (`[[2026/20261103#^id]]`), where gf reads the source-text cache and gg reads the live document. A disagreement anywhere else is a bug.
7. gf's source-text freshness fix (refresh an already-cached entry on `metadataCache` `changed`) also serves gg's Reading-view pills. Keep exactly one such fix; do not add a second invalidation path.
8. Once both have landed, run both unit suites (`test-ledger-tools-off-clock-link-chips.cjs`, `test-ledger-tools-event-link-times.cjs`). Confirm gg's EP3 (`pill link off`) and gf's OP5 (◐/🔓/🔑 still paint, no ring) with both hosts on one row.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-gf.1](bob-cli-gf.1.md) | Authoritative display contract (bob-cli) | ✓ closed | small | 2026-11-03 | 1 | 1 |
| [bob-cli-gf.2](bob-cli-gf.2.md) | The chip in bob-ledger-tools (bob-plugins) | ✓ closed | medium | 2026-11-03 | 1 | 1 |
| [bob-cli-gf.3](bob-cli-gf.3.md) | Real-Obsidian e2e and visual review (bob-plugins, bob-cli) | ◐ in_progress | medium | 2026-11-03 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-gf: Off-clock link chips — show the `#off` chip after ledger Task Links to off-clock tasks [in_progress]"]
    n1["bob-cli-gf.1: Authoritative display contract (bob-cli) [closed]"]
    n2["bob-cli-gf.2: The chip in bob-ledger-tools (bob-plugins) [closed]"]
    n3["bob-cli-gf.3: Real-Obsidian e2e and visual review (bob-plugins, bob-cli) [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n1 -.-> n2
    n2 -.-> n3
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-gf.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-gf.1/README.md) | [bob-cli-gf.1](bob-cli-gf.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-gf.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-gf.2.md) | [bob-cli-gf.2](bob-cli-gf.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-gf.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-gf.3/README.md) | [bob-cli-gf.3](bob-cli-gf.3.md) | 0 |
| [bbugyi200.apollo.bob-cli-gf.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-gf.land/README.md) | [bob-cli-gf](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`5f35f0b`](https://github.com/bobs-org/bob-cli/commit/5f35f0b306de8a8155f7b6ba6ac5932aecc748d8) | docs(off-clock-chips): add ledger off-clock link chip display contract | [bob-cli-gf.1](bob-cli-gf.1.md) | 2026-11-03 10:10:19 EST |
| bob-plugins | [`bob-plugins@23d401b`](https://github.com/bobs-org/bob-plugins/commit/23d401bc95fca3e92baed6a5565a98833a4b653b) | feat(ledger-tools): add off-clock link chips | [bob-cli-gf.2](bob-cli-gf.2.md) | 2026-11-03 10:50:05 EST |
