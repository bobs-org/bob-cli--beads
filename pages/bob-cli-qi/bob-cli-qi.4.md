# Bead: bob-cli-qi.4 — Real-Obsidian takeover acceptance and family screenshot review

[Bead Pages](../README.md) / [bob-cli-qi](README.md) / bob-cli-qi.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1gn](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1gn.md) · **Assignee:** `bob-cli-qi.4` · **Size:** medium
**Created:** 2026-11-26 10:06:12 EST · **Closed:** 2026-11-26 12:48:47 EST
**Plan:** [202611/bank\_hub\_demotion.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_hub_demotion.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:290bf602385934c8b83ee465 | attached via sase artifact create --bead |
| related | file:explicit:2a125acea859ceb79722a65c | attached via sase artifact create --bead |
| related | file:explicit:9bc0eacb4d944023db5b3888 | attached via sase artifact create --bead |
| related | file:explicit:c4c6acced7cb004fabf26e32 | attached via sase artifact create --bead |
| related | file:explicit:cdd6ba05e0b402a23c048298 | attached via sase artifact create --bead |
| related | file:explicit:dce3a74989f86e48da93715d | attached via sase artifact create --bead |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

takeover-proof: run the production-adapter matrix in isolated real Obsidian against a master-built bob, covering area, inbox, project, and the single-owner bank card. Prove fail-open, focus, routing, and ^prj integrity, and repair defects this work caused. Review light/dark and narrow/wide screenshots across the card family and retain all evidence.

## Notes

[2026-11-26T16:07:45Z · bob-cli-qi.4] Takeover-proof progress: built master bob 0.6.0 @478d5233 (debug binary verified). Fixed a bank single-owner defect left by qi.3: `arbitration.owner` ReferenceError in `bankSetupLiveDecorations` fallback (plugins/bob-ledger-tools/src/248c-plugin-bank-setup-hosts.js) crashed bank Live Preview owns-row path; restored the pre-arbitration anchor line and dropped the stale Area-owns-bank comment. Rebuilt bundle (`npm run build`, `build:check` clean, zero `arbitration` refs in main.js). Affected suite test-ledger-tools-property-card-ownership.cjs: 13/13 pass; bank-focused suites (home-card-model/host, foot-adapters, frontmatter-ownership, editor entrypoints/settings): 106/106 pass; offline runner self-tests: 18/18 takeover + 5/5 home-cards.

[2026-11-26T16:07:54Z · bob-cli-qi.4] PROPOSED FOLLOW-UP: npm test on bob-plugins master (8e6a5a61+) has 2 pre-existing failures that reproduce identically on the pristine tree without the qi.4 fix (verified via git stash + rebuild): (1) test-block-id-prompt-pomodoro-theme-write.cjs "Enter merges the current type into the destination name" expects [[Tasks#^ship]]; (2) test-task-status-cycler-reference-lifecycle.cjs "post-close finalizer runs one gated plan before reference retirement" has an extra snoozedPruned:0 key. Both are in snoozed/pomodoro surfaces outside the bank single-owner scope. Repro: cd sase/repos/linked/bob-plugins && node --test <file>.

[2026-11-26T17:02:58Z · bob-cli-qi.4] Takeover-proof recovery: staged monitor 535fgm never launched its process (53m in staged state, no output, no /tmp/bob-cli-qi4 on athena) and hit its 50m timeout. Stopped it and re-staging the same two-runner matrix fresh; committing the verified bank arbitration-leftover fix first so the rerun tests a clean tree.

[2026-11-26T17:48:19Z · bob-cli-qi.4] Takeover-proof evidence (fix tree @4e0a8fd0 + uncommitted 248c arbitration-leftover fix, bob 0.6.0 master debug build 6bd44880): takeover runner full profile 62/63, verdict GO (reading only; live preview keeps per-row hiding) — all reading+both checks pass, bytes-unchanged passes, 46 screenshots captured. Single live failure varies by run (live-slow-reparse-keeps-card twice, live-autosave-keeps-ownership once): record-foot text churn during live autosave/reparse, ownership held throughout, bytes unchanged — recorded as follow-up, not this work. Home-cards runner 53/60 with the same 7 baseline fails on fix and pristine trees; aborts before screenshots (0 shots) on runner-error project-folds timeout — recorded as follow-up. Reviewed bank live+reading x light/dark x wide/narrow (single Bank Card BANK·HOME·CASH, one title, one foot, Setup folded, no Area card, narrow wraps clean), record-live and album-live wide: all pass, no visual drift. Artifacts: file:explicit:290bf602385934c8b83ee465 (takeover report), file:explicit:9bc0eacb4d944023db5b3888 (takeover log), file:explicit:cdd6ba05e0b402a23c048298 (46 shots tar), file:explicit:dce3a74989f86e48da93715d + file:explicit:2a125acea859ceb79722a65c + file:explicit:c4c6acced7cb004fabf26e32 (homecards report/log/empty-shots tar). Staged monitor 535fgm never launched its process (stuck staged to timeout); work ran inline via durable tool runs 76d10a/1a1b4d/8253d95/f43cbbe/53ee4f/cc763b99/728d2c.

[2026-11-26T17:48:32Z · bob-cli-qi.4] PROPOSED FOLLOW-UP: record-foot text churn fails one live takeover check per run (live-slow-reparse-keeps-card or live-autosave-keeps-ownership): the record probe re-renders resolved relation rows (Corner Bistro 1-2 of 2) across ~60-180 samples during live autosave/slow-reparse while ownership holds and bytes stay unchanged. Reproduces identically on pristine master (tool run 8253d95), so not caused by qi.4. Prime suspect is qi.3 8e6a5a61 240r whole-scope-release revert (replaced pane-local prune of disconnected mounts); reinstating the prune would reverse a settled sibling-phase decision, so left for triage — decide whether the keeps-card text-stability expectation or the re-resolution behavior gives.

[2026-11-26T17:48:37Z · bob-cli-qi.4] PROPOSED FOLLOW-UP: home-cards runner 53/60 on fix and pristine trees alike (tool runs 728d2c fix-tree vs cc763b99 pristine, identical 7): reading goal decoration missing on scheduled/done/canceled ^prj lines, area/project cursor not on expected body line (drawnTop matches, line text differs), matrix-spawns-no-home-card-bob flags 2 unknown:__catalog --protocol 1 spawns as home-card-triggered, runner-error project-folds timeout aborts before screenshots (0 shots, so no area/project card visuals retained). Repro: cd sase/repos/linked/bob-plugins && OBSDIAN_TASKS_PLUGIN_DIR=~/bob/.obsidian/plugins/obsidian-tasks-plugin xvfb-run -a node scripts/obsidian-home-cards-e2e.cjs -e /snap/obsidian/current/app/obsidian.

[2026-11-26T17:48:47Z · bob-cli-qi.4] Takeover-proof done: bank single-owner verified (own-bank-live/reading, props-v1-only-owned, pane-path-lifecycle, generic-editor-gestures pass; reviewed single Bank Card in live+reading x light/dark x narrow/wide, no Area card), full matrix 62/63 with partial GO (reading only). Remaining 1 live check (record-foot churn), 7 home-cards checks, and 2 npm suites fail identically on the pristine base tree — recorded as PROPOSED FOLLOW-UP notes, not this work. Fixed the qi.3 arbitration leftover (248c fallback ReferenceError) with unit+build:check green. Evidence in 6 bead artifacts.

## Dependencies

- **Depends on:** [bob-cli-qi.1](bob-cli-qi.1.md) ✓ · ⧖ 2026-11-26
- **Depends on:** [bob-cli-qi.2](bob-cli-qi.2.md) ✓ · ⧖ 2026-11-26
- **Depends on:** [bob-cli-qi.3](bob-cli-qi.3.md) ✓ · ⧖ 2026-11-26
- **Blocks:** [bob-cli-qi.6](bob-cli-qi.6.md) ◐ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-qi.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-qi.4.md) | [bob-cli-qi.4](bob-cli-qi.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@19e895f`](https://github.com/bobs-org/bob-plugins/commit/19e895f0993f09816cf5216ff5585fa258a9be3f) | fix(plugins): drop stale bank/area arbitration anchor in live fallback | [bob-cli-qi.4](bob-cli-qi.4.md) | 2026-11-26 12:51:31 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:research.6k.cld][1] | Check phase progress to plan parallel prose/notebook card work | 1 |
| read-by | [agent:research.6k.gem][2] | Inspect in-progress phase details and progress notes of qi and qj epics | 1 |
| read-by | [agent:research.6k.grk][3] | Need remaining takeover-proof work to judge whether new card species can land in parallel | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.6k.cld/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.6k.gem/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.6k.grk/README.md

<!-- sase:referenced-by:end -->
