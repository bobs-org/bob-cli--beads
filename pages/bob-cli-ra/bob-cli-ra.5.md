# Bead: bob-cli-ra.5 — Real-Obsidian link-walk acceptance with screenshot review

[Bead Pages](../README.md) / [bob-cli-ra](README.md) / bob-cli-ra.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.6o.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.6o.linker.w0.md) · **Assignee:** `bob-cli-ra.5` · **Size:** medium
**Created:** 2026-11-27 15:01:37 EST · **Closed:** 2026-11-28 06:46:55 EST
**Plan:** [202611/tree\_note\_link\_walks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/tree_note_link_walks.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:4654832fef8772cf15dec9b6 | attached via sase artifact create --bead |
| related | file:explicit:764f44316c7ca8b3a96336db | attached via sase artifact create --bead |
| related | file:explicit:78352ade714018b409dcdcac | attached via sase artifact create --bead |
| related | file:explicit:86ab1d0f0b9a6c45b2931196 | attached via sase artifact create --bead |
| related | file:explicit:a1ed81b79efe17d52d0bc55e | attached via sase artifact create --bead |
| related | file:explicit:ced624aef339f4a3cd0c942c | attached via sase artifact create --bead |

_Plus 5 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

acceptance: add a scratch-vault runner for all eight keys on all four types, check that rail, footer, and keys agree, run the floor, passivity, console-error, and perf checks plus re-validation, review every screenshot on athena, and reach GO.

## Notes

[2026-11-28T01:30:07Z · bob-cli-ra.5--6] FAILURE EVIDENCE — NO-GO. The 2026-11-28 01:09:12–01:12:52 UTC gate run passed `npm run build:check`, but `npm run test:unit` reported 10,458 tests: 10,452 passed, 1 failed, 5 skipped. The sole failure remains `navigation runs all canonical snooze add and drop mutation vectors` (`snooze-add-resnooze-replaces-history daily postimage`). This misses the required exact baseline of 10,451 passed, 1 failed, 5 skipped. The net extra passing test was added by unrelated commit `2333aa72` in `scripts/test-ledger-tools-cabinets-absorption.cjs`; the test suite and strict count were left unchanged. `bob plugins sync` succeeded without force (2 copied, 32 unchanged). The gate stopped before the Athena refresh and fresh captures.

The only available acceptance report is the earlier run1 report, which failed while waiting for the `The stop changed` notice. The current runner includes the resolver-settle wait (`1834c283`) and direct notice-call evidence (`145b4a3d`), but it has not produced a fresh report; run2 is absent. No final screenshot set was copied or visually reviewed. Evidence artifacts: `file:explicit:86ab1d0f0b9a6c45b2931196` (gate diagnosis) and `file:explicit:4654832fef8772cf15dec9b6` (prior run1 report). The phase remains in progress.

PROPOSED FOLLOW-UP: Run the acceptance gates against the phase's intended source and test inventory while retaining the full unit suite and exact-count guard. Once the exact baseline passes, perform the non-force plugin sync, refresh Athena scripts/plugins without deleting acceptance results, rerun both captures, then copy and visually inspect every final PNG before deciding GO/NO-GO.

[2026-11-28T11:46:11Z · bob-cli-ra.5] VERDICT: GO. Source: bob-plugins base 91db00d3 plus this phase's commit. The commit fixes the tree provider (296ha): group stops now carry the parent label as shortLabel, and step and parent stops keep the landing. That bumps Bob Ledger Tools 1.175.0 → 1.175.1, regenerates the docs inventory, and adds unit asserts. It also hardens the runner (convergent start probe, fixture restore before captures, a narrow group-label check, and retrying teardown). Two real-Obsidian runs on athena under xvfb-run each passed 142/142 checks: 32 key landings; rail = footer = keys on all 4 types; inline-code and authored nav lines; 5 malformed-parent reasons; reparent, rename, and ^prj live updates with no card rebuild; floor last on tree, day, and record cards through toggles, repaints, and Reading; "The stop changed — try again" on a deleted stop; 0 vault writes and 0 bob spawns (hash unchanged); 0 console errors. Perf: index build 3.0 / 4.3 ms. Reading paint on the 64-child host, median with rail vs stubbed: 139.2 vs 137.2 ms (ratio 1.0146) and 136.9 vs 138.7 ms (ratio 0.9870); no long tasks over 50 ms. All 24 captures were inspected (light, dark, and forced colors at 420 px; Live Preview and Reading); every verdict is pass and the beauty checklist is all green. npm test: 10,459 pass, 1 fail (pre-existing on the clean base, see the follow-up), 5 skip; perf 28/28. build:check is green. bob plugins sync succeeded without -F (3 copied). Evidence: review file:explicit:a1ed81b79efe17d52d0bc55e, run1 file:explicit:764f44316c7ca8b3a96336db, run2 file:explicit:ced624aef339f4a3cd0c942c, screenshots file:explicit:78352ade714018b409dcdcac. For the docs phase: document that tree group stops carry shortLabel = parent label (like calendar and record group stops).

[2026-11-28T11:46:23Z · bob-cli-ra.5] PROPOSED FOLLOW-UP: [ci] Fix the failing cabinets-chrome album Schema test. `album Schema is closed when healthy and still resurfaces on problems` (scripts/test-ledger-tools-cabinets-chrome.cjs:291) fails on clean bob-plugins master 91db00d3: albumHeaderIsExpanded("eat.md", { schemaInvalid: true, issues: [error] }) returns false. It was likely introduced by 15c2410d ("cabinets start closed, configurable per card type"). It is the only npm test failure, and it reproduces identically without this phase's changes.

[2026-11-28T11:46:29Z · bob-cli-ra.5] PROPOSED FOLLOW-UP: [bug] The walker footer clips its left edge in narrow windows. At a 420 px Obsidian window, the links footer (status bar) is cut on the left for project, notebook, and prose notes ("e Links", "ks · goo …"). freshnessFooterFit (bob-ledger-tools src/121-freshness-footer-paint.js) compares only the footer item's own scrollWidth with its clientWidth, so it never sheds when the status bar container overflows. The code is shared by all walker footers. Evidence: ra.5 screenshots file:explicit:78352ade714018b409dcdcac.

[2026-11-28T11:46:35Z · bob-cli-ra.5] PROPOSED FOLLOW-UP: [bug] The project card's title-block icon tile is clipped on its right edge. In every ra.5 project capture (light, dark, and forced colors; Live Preview and Reading; 420 px), the project card icon tile is cut by the title column, while the area, notebook, and prose tiles render whole. No icon or title-block CSS changed in the rail or cards commits, so the bug predates this epic. Evidence: file:explicit:78352ade714018b409dcdcac.

[2026-11-28T11:46:55Z · bob-cli-ra.5] VERDICT: GO. Verified on athena: two real-Obsidian runs each passed 142/142 checks. They covered the keys, rail/footer/key agreement, the floor on tree, day, and record cards, live updates, stale-stop re-validation, passivity, zero console errors, and perf (ratios 1.0146 and 0.9870, no long tasks). All 24 captures were inspected and pass. I fixed the narrow group-arm label in the tree provider (Bob Ledger Tools 1.175.1) and hardened the runner. build:check is green. npm test has only the pre-existing album Schema failure, which reproduces on clean 91db00d3 and is recorded as a follow-up. bob plugins sync succeeded without -F. Evidence artifacts are on the bead.

## Dependencies

- **Depends on:** [bob-cli-ra.4](bob-cli-ra.4.md) ✓ · ⧖ 2026-11-27
- **Blocks:** [bob-cli-ra.6](bob-cli-ra.6.md) ✓ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ra.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ra.5/README.md) | [bob-cli-ra.5](bob-cli-ra.5.md) | 5 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@7843342`](https://github.com/bobs-org/bob-plugins/commit/7843342216c269079fece729db68c33b175793e3) | test(acceptance): add real tree-walk Obsidian runner | [bob-cli-ra.5](bob-cli-ra.5.md) | 2026-11-27 19:04:46 EST |
| bob-plugins | [`bob-plugins@d83ffbe`](https://github.com/bobs-org/bob-plugins/commit/d83ffbebad69e1ec9e5ce8d8661648fbcb5a696d) | fix(test): scope tree-walk long-task samples | [bob-cli-ra.5](bob-cli-ra.5.md) | 2026-11-27 19:32:23 EST |
| bob-plugins | [`bob-plugins@1834c28`](https://github.com/bobs-org/bob-plugins/commit/1834c28322b0e7c7e687625b7e034254e52f49b1) | fix(acceptance): wait for stale link resolution | [bob-cli-ra.5](bob-cli-ra.5.md) | 2026-11-27 19:58:17 EST |
| bob-plugins | [`bob-plugins@145b4a3`](https://github.com/bobs-org/bob-plugins/commit/145b4a3d1ed88c1cabe78029ab9b6a08c3eff695) | test(acceptance): record stale rail notice evidence | [bob-cli-ra.5](bob-cli-ra.5.md) | 2026-11-27 20:10:16 EST |
| bob-plugins | [`bob-plugins@d0ddd12`](https://github.com/bobs-org/bob-plugins/commit/d0ddd12c61c09a511d6eb32ea76a51361d6cc099) | fix(ledger-tools): name parents on narrow tree group arms and reach tree-walk acceptance GO | [bob-cli-ra.5](bob-cli-ra.5.md) | 2026-11-28 06:47:43 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ra.5][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-ra.5--2][1] | Need current assigned epic scope, status, and notes before recording acceptance evidence | 1 |
| read-by | [agent:bob-cli-ra.5--5][1] | Inspect requested acceptance-phase status and record evidence | 1 |
| read-by | [agent:bob-cli-ra.6][2] | Need acceptance GO evidence: plugin versions, perf numbers, commit | 1 |
| read-by | [agent:g7.f1--code][3] | Check whether ra.5 closed and landed the tree-walk runner we just fetched | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ra.5.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ra.6/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.g7.f1.md

<!-- sase:referenced-by:end -->
