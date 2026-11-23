# Bead: bob-cli-pf.4.1.7.4 — Real-Obsidian acceptance for panes, entry points, and visuals

[Bead Pages](../README.md) / [bob-cli-pf.4.1.7](bob-cli-pf.4.1.7.md) / bob-cli-pf.4.1.7.4

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pf.4.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.4.1.land.md) · **Assignee:** `bob-cli-pf.4.1.7.4` · **Size:** medium
**Created:** 2026-11-23 03:09:55 EST
**Plan:** [202611/property\_editor\_landing\_repairs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/property_editor_landing_repairs.md)

## Description

acceptance-surfaces: cover panes, history reopen, YAML Done, close keys, unload, every entry point, and reviewed light/dark narrow/wide screenshots on athena; document the run in validation.md.

## Notes

[2026-11-23T13:56:38Z · bob-cli-pf.4.1.7.4] Local work complete before Athena: CSS selected/locked row grid, is-selected/is-locked paint, surfaces harness (panes/stale/history/YAML/close/entry/unload/visuals), validation.md walkthrough. Focused 29/29. npm validate pass. bob plugins sync copied ledger-tools main.js+styles.css (no -F). npm test 9028 pass/4 fail/5 skip: km+io isolation-pass (bob-cli-km, bob-cli-io); task_reqs README twin-copy drift and docs-check task-drawers nav (bob-cli-ph.1) are pre-existing. Next: real Obsidian e2e on Athena, PNG review, artifacts, epic-symbols, close.

[2026-11-23T14:09:53Z · bob-cli-pf.4.1.7.4--1] Athena monitor 0zgqpe failed before Obsidian: rsync --exclude /sase omitted tracked sase/memory files, so BOB_CLI_DIR was dirty and no report/PNGs were produced. Retrying with git checkout -f after rsync, excluding the 8.8G .build tree.

[2026-11-23T14:24:16Z · bob-cli-pf.4.1.7.4--2] Monitor g3zdqz reached Obsidian with plugins ready, then timed out waiting for application window focus. Report: focused=true, active=false, activeDocumentUrl=about:blank, activePath=null, documentEditors=0. Failure PNG is an empty New tab (no property editor, so no clipping/focus-ring/selected-row/locked-row). Harness now destroys the leftover about:blank Electron window and clicks the tab strip; Athena xvfb-run starts xfwm4. Focused unit tests 8/8. Retrying Athena instead of closing.

## Dependencies

- **Depends on:** [bob-cli-pf.4.1.7.3](bob-cli-pf.4.1.7.3.md) ✓ · ⧖ 2026-11-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pf.4.1.7.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.4.1.7.4.md) | [bob-cli-pf.4.1.7.4](bob-cli-pf.4.1.7.4.md) | 5 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@1408a83`](https://github.com/bobs-org/bob-plugins/commit/1408a834014eb1dfb1f856f5f9c32f73356d07b3) | feat(property-editor): distinguish selected and locked rows | [bob-cli-pf.4.1.7.4](bob-cli-pf.4.1.7.4.md) | 2026-11-23 09:00:34 EST |
| bob-plugins | [`bob-plugins@e06f85e`](https://github.com/bobs-org/bob-plugins/commit/e06f85e3462eb76b494da2fcfcd5c143137a36d3) | fix(e2e): close Obsidian's blank startup window before Property Editor | [bob-cli-pf.4.1.7.4](bob-cli-pf.4.1.7.4.md) | 2026-11-23 09:25:53 EST |
| bob-plugins | [`bob-plugins@2a78691`](https://github.com/bobs-org/bob-plugins/commit/2a7869183f19a1d3cf6b6277688f8c84f4c51743) | fix(property-editor): keep requested edit key across empty cache | [bob-cli-pf.4.1.7.4](bob-cli-pf.4.1.7.4.md) | 2026-11-23 09:45:07 EST |
| bob-plugins | [`bob-plugins@337977b`](https://github.com/bobs-org/bob-plugins/commit/337977b0c6ab5d4dcb2fa206d1d8de0e75ef955a) | fix(e2e): match Property Editor stale-refusal copy | [bob-cli-pf.4.1.7.4](bob-cli-pf.4.1.7.4.md) | 2026-11-23 09:56:40 EST |
| bob-plugins | [`bob-plugins@b75ed48`](https://github.com/bobs-org/bob-plugins/commit/b75ed48930150fe5268283d3d92b0921187fa65d) | fix(e2e): match quoted YAML on Property Editor stale-refusal bytes | [bob-cli-pf.4.1.7.4](bob-cli-pf.4.1.7.4.md) | 2026-11-23 10:06:17 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pf.4.1.7.4--2][1] | Diagnose Athena Property Editor e2e focus timeout before fixing harness | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.4.1.7.4.md

<!-- sase:referenced-by:end -->
