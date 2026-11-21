# Bead: bob-cli-oj.5.1.3 — Grouped record walk rail and the album card's "walks by" pill

[Bead Pages](../README.md) / [bob-cli-oj.5.1](bob-cli-oj.5.1.md) / bob-cli-oj.5.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-oj.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-oj.5.md) · **Assignee:** `bob-cli-oj.5.1.3` · **Size:** medium
**Created:** 2026-11-21 12:21:10 EST · **Closed:** 2026-11-21 13:23:20 EST
**Plan:** [202611/group\_rail.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/group_rail.md)

## Description

record-rail: give grouped record walk rails the kit group row in place of the whole-walk thumb track, reword the count tooltip, activate arms through the group commands with re-validation, add the album card's `· walks by <Field>` pill, test it, update docs/record-card.md and docs/albums.md, then build, test, bump, commit, and sync.

## Notes

[2026-11-21T18:22:59Z · bob-cli-oj.5.1.3] PROPOSED FOLLOW-UP: Load-sensitive Ledger wall-time asserts failed again only under the parallel full npm test on the merged tree (bob-plugins origin/master 63e2f64 + record-rail): test-ledger-tools-frees-marks.cjs:481 (40 ms vs 25 ms budget) and test-ledger-tools-keep-moving-marks.cjs:236 (1500 resident count took 2141 ms); both files pass in isolation. Same class as the follow-up already recorded on bob-cli-oj.1 and bob-cli-oj.5.1.1; moving wall-time asserts to the serial perf lane would stop these.

[2026-11-21T18:23:20Z · bob-cli-oj.5.1.3] record-rail landed in bob-plugins Ledger Tools 1.152.0 (merged on origin/master 63e2f64 after calendar-rail took 1.151.0; commit via this turn's finalizer). New 242va BobLedgerToolsRecordWalkGroupRailMixin: walk.groupRail from walkMode.links v7 (else navGroupsResolve), gated on a healthy walk over >=2 occupied groups (ungrouped/single-group/syncing/grouping_unavailable never ask the resolver and keep today's rail); 242u appends the kit group row in place of bob-record-walk-track (arms '« <group> · <head>' / '<group> · <head> »', ↺ on wraps, ghost heads dotted '· not in vault', centre choice label + 'k of n' + member ticks), count tooltip 'By <Field>, then title · wraps around'; 242v recordWalkFor attaches it and recordWalkOptions gains handlers.groupOpen (ghost = notice + album sync; modified click on exists = Markdown open; plain click re-reads the pane text, re-validates target/path/state, refuses with 'The group stop changed — try again' + repaint, else focuses the card's leaf and runs open-prev/next-group-link; no-Nav fallback opens via recordWalkOpen); 242k one line attaches it to the sheet model's walk; 242ia adds the group rail to recordSheetWalkSignature. Album pill: 241u walkBy/walkByLabel in model + signature, 241x appends '· walks by <Field>' span with tooltip on healthy folded lines only. CSS in its own 'Record walk group row (bob-cli-oj record-rail)' block after the group-row block. Docs: docs/record-card.md and docs/albums.md (both <3000 words). Verified: new scripts/test-ledger-tools-record-walk-group-rail.cjs 12/12 (registered in test:unit) + album-header 41/41 (new pill test); record-walk, record-sheet, nav-groups, group-row, intention group-rail suites green; npm run build:check green; full npm test on the merged tree 8220/8226 with only two wall-time flakes (frees-marks:481, keep-moving-marks:236) that pass in isolation (PROPOSED FOLLOW-UP noted); docs:check fails only on base budget errors (nav-hotkeys reference 6247/6000, vault-format 6037/6000 = bob-cli-oc). Throwaway real-Obsidian render (light/dark x 375/900 + forced-colors) checked: group row replaces the track, narrow collapses to '« 🛑 … · 2/3 · 🏁 Conclusion »', ghost arm dotted; note for rail-proof: under forced-colors the kit's transparent 1px border makes exists group arms draw a solid box (kit-wide, not record-specific). bob plugins sync deployed 1.152.0; bob plugins list --no-pull shows bob-ledger-tools 1.152.0 synced.

## Dependencies

- **Depends on:** [bob-cli-oj.5.1.1](bob-cli-oj.5.1.1.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-oj.5.1.4](bob-cli-oj.5.1.4.md) ◐ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-oj.5.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.3/README.md) | [bob-cli-oj.5.1.3](bob-cli-oj.5.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@2aa877c`](https://github.com/bobs-org/bob-plugins/commit/2aa877ce6064c4679077fadd77c58f530ea8bdd3) | feat(ledger-tools): add the grouped record walk rail and the album walks-by pill | [bob-cli-oj.5.1.3](bob-cli-oj.5.1.3.md) | 2026-11-21 13:24:17 EST |
