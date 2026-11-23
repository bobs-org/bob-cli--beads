# Bead: bob-cli-on.11.1.7 — Repair the Obsidian requirement close card and prove it end to end

[Bead Pages](../README.md) / [bob-cli-on.11.1](bob-cli-on.11.1.md) / bob-cli-on.11.1.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-on.11.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.11.1.land.md) · **Assignee:** `bob-cli-on.11.1.7.land`
**Created:** 2026-11-22 20:02:19 EST · **Closed:** 2026-11-23 00:53:38 EST
**Plan:** [202611/obsidian\_req\_close\_card\_repairs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/obsidian_req_close_card_repairs.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/obsidian_req_close_card_repairs.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/obsidian_req_close_card_repairs.md

<!-- sase:links:end -->

## Description

Make explicit requirement verdicts, jump pins, staleness guards, counted and idless closes actually work on the Obsidian managed Done card, prove every path through public entry points and real Obsidian, and finish the contract docs.

## Notes

[2026-11-23T05:20:55Z · bob-cli-on.11.1.7.land] LAND FOLLOW-UP TRIAGE: both immediate children have no PROPOSED FOLLOW-UP entries. Reviewed every note on parent phases on.11.1.1-.6: .1 #1, .3 #1, .5 #2, .6 #1 event-link-times -> existing bob-cli-km; .2 #1, .3 #1, .6 #1 frees-marks -> existing bob-cli-io. Used sase_new_task, checked same-type all-status matches, last-week task sweep, and all 20 active epic scopes; these nodes predate this epic and no active epic causally owns their load-only timing defects. Added attributed supplementary notes on km/io; declined duplicate task creation and +1 because no new independent flake reproduction. Parent on.11.1 notes #3-4 documentation headroom stays with existing bob-cli-ob: plugin-apis exceeded its advisory cap before this epic (8401/8000), prior growth is already corroborated, and required API facts must remain. No new CI task or API-fact deletion. New mixed-verdict Undo defect is epic work and will be repaired by the landing tale, not deferred as a task.

[2026-11-23T05:23:03Z · bob-cli-on.11.1.7.land] LAND VERIFICATION INCOMPLETE at bob-plugins e1ed13f and bob-cli 39661003: reviewed both child scopes/all notes, parent on.11.1 and all six phases/all notes, approved plans, repair commits 44db8ce/69a7ca0/0bddc2e/21331f3/e1ed13f and bf005290, and actual production wiring. 244 focused SP/RV/picker/carry/receipt/integration/public-path tests passed; an extra idless Carry+pin probe passed. Confirmed prior monitor 16hpvrb8fdz2 exit 0 and six real-Obsidian scenarios, and current nav 2.107.0/cycler 1.58.1 synced. Did not rerun live E2E or full gates this turn. Post-start property-card/props/highlights commits and ef640fde Mac consumer docs have no identified integration conflict. No epic-symbol entries for on.11.1.7, on.11.1, on.11. Remaining reproduced epic defect: one card selecting ordinary Offered Done and requirement Handles empty input Drop with a reason in Tasks.md applies both but immediate real nav restoreGuardedSnapshots returns false. Undo after contains the pre-Drop requirement line, not current dropped line/Cancel Log. 137-plugin-successor-project.js composes reqRestores before closeRestores even though offer-close writes happen first; 198g last-after semantics overwrite the final req postimage with the older offer-close postimage. Introduced by parent c91ebae, missed by child test 12 (req-only) and test 6 (ordinary pick rather than close). Repro must install real navHarness.helpers.createCancelApi and assert the ordinary close descriptor accepts; otherwise a refused close falsely passes exclusion tests. A small tale will fix composition, add mixed public-path Undo coverage, verify/deploy, and finish on.11.1.7 -> on.11.1 -> phase on.11 normally without closing on.

[2026-11-23T05:53:14Z · bob-cli-on.11.1.7.land] LAND COMPLETE (mixed-undo tale): compose fix in 137-plugin-successor-project.js now reqCloseIntegrationComposeRestores([...closeRestores, ...reqRestores]) so first-before/last-after keep the post-initiating-close preimage and the final req/pull-in after. 137 is 904 lines. Public-path harness installs createCancelApi(); test 10 actually closes Offered; tests 12a-12d cover mixed Drop, Carry+pull-in, postimage refuse, and partial family. node --test scripts/test-task-status-cycler-req-close-public-paths.cjs 25/25 after npm run build. Live e2e node scripts/obsidian-req-close-card-e2e.cjs PASS all 6 (mixed 7th skipped as impractical). Plugin docs:check and bob-cli just docs-check exit 0. npm test 8912 pass / 3 fail / 4 skip: km and io 25ms nodes fail under load and pass isolated; period-notes stub-fill is date-pin CI, corroborated +1 on bob-cli-pm (not a flake). sase tool run check (just check) succeeded 568s id ab245f33e7288778f9f38dd7e929f822. Deployed bob plugins sync --repo opened bob-plugins -p task-status-cycler without -F; list: cycler 1.58.1 deployed from this uncommitted e1ed13f, nav 2.107.0 synced enabled. Ledger-tools drift is concurrent other workspace. Integration since baseline: plugins a5c2269/8ac4790/bb57281/c8deb53 property-card/ledger-tools; bob-cli 39661003/4fed68fc/15225a6a/ef640fde/29d7fec7/3e480e4a/33f6d08d props/highlights/Mac docs. No conflict with mixed Undo. Follow-ups remain km/io/ob; p8 is separate project-scope count. epic-symbols empty for on.11.1.7, on.11.1, on.11. justfile has no symvision recipe.

[2026-11-23T05:53:38Z · bob-cli-on.11.1.7.land] Mixed-undo tale complete. 137 composes closeRestores then reqRestores; public-path 25/25 including mixed Drop/Carry+pull-in/postimage refuse/partial; live e2e 6/6; just check succeeded (sase tool run check ab245f33e7288778f9f38dd7e929f822, 568s); docs gates pass; cycler deployed without -F (1.58.1 from uncommitted e1ed13f), nav 2.107.0 synced. Flakes km/io isolated pass; period-notes +1 on bob-cli-pm. Follow-ups stay km/io/ob; p8 separate. No epic-symbols. Children .1 and .2 already closed. justfile has no symvision recipe.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.11.1.7.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.11.1.7.land.md) | [bob-cli-on.11.1.7](bob-cli-on.11.1.7.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`9c9c972`](https://github.com/bobs-org/bob-cli/commit/9c9c972c2873a23bb62ea44d89b756fd37823cbf) | docs(task-requirements): cover mixed close-card Undo in one gesture | [bob-cli-on.11.1.7](bob-cli-on.11.1.7.md) | 2026-11-23 00:56:01 EST |
| bob-cli--plans | [`bob-cli--plans@8eb9c65`](https://github.com/bobs-org/bob-cli--plans/commit/8eb9c6521c4471844f62ca84055af8dc4a205968) | docs(plans): mark req close-card mixed-undo landing done | [bob-cli-on.11.1.7](bob-cli-on.11.1.7.md) | 2026-11-23 00:58:11 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-on.11.1.7.1][1] | Need parent epic DECISIONS and phase design | 2 |
| read-by | [agent:bob-cli-on.11.1.7.2--3][2] | Need the parent child-epic scope and the expected phase closeout evidence | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.11.1.7.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.11.1.7.2.md

<!-- sase:referenced-by:end -->
