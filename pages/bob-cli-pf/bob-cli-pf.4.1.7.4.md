# Bead: bob-cli-pf.4.1.7.4 — Real-Obsidian acceptance for panes, entry points, and visuals

[Bead Pages](../README.md) / [bob-cli-pf.4.1.7](bob-cli-pf.4.1.7.md) / bob-cli-pf.4.1.7.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pf.4.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.4.1.land.md) · **Assignee:** `bob-cli-pf.4.1.7.4` · **Size:** medium
**Created:** 2026-11-23 03:09:55 EST · **Closed:** 2026-11-23 11:19:22 EST
**Plan:** [202611/property\_editor\_landing\_repairs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/property_editor_landing_repairs.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:36d3fab3790612136e5f0ca8 | attached via sase artifact create --bead |
| related | file:explicit:49ee66906e8ea8acb9a84f58 | attached via sase artifact create --bead |
| related | file:explicit:5920b45f8a4e4c729e2d738e | attached via sase artifact create --bead |
| related | file:explicit:8168a7fbdad3b7c39330defb | attached via sase artifact create --bead |
| related | file:explicit:848daf017651f258b7137e00 | attached via sase artifact create --bead |
| related | file:explicit:bdd1744c20a50aa51751a550 | attached via sase artifact create --bead |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

acceptance-surfaces: cover panes, history reopen, YAML Done, close keys, unload, every entry point, and reviewed light/dark narrow/wide screenshots on athena; document the run in validation.md.

## Notes

[2026-11-23T13:56:38Z · bob-cli-pf.4.1.7.4] Local work complete before Athena: CSS selected/locked row grid, is-selected/is-locked paint, surfaces harness (panes/stale/history/YAML/close/entry/unload/visuals), validation.md walkthrough. Focused 29/29. npm validate pass. bob plugins sync copied ledger-tools main.js+styles.css (no -F). npm test 9028 pass/4 fail/5 skip: km+io isolation-pass (bob-cli-km, bob-cli-io); task_reqs README twin-copy drift and docs-check task-drawers nav (bob-cli-ph.1) are pre-existing. Next: real Obsidian e2e on Athena, PNG review, artifacts, epic-symbols, close.

[2026-11-23T14:09:53Z · bob-cli-pf.4.1.7.4--1] Athena monitor 0zgqpe failed before Obsidian: rsync --exclude /sase omitted tracked sase/memory files, so BOB_CLI_DIR was dirty and no report/PNGs were produced. Retrying with git checkout -f after rsync, excluding the 8.8G .build tree.

[2026-11-23T14:24:16Z · bob-cli-pf.4.1.7.4--2] Monitor g3zdqz reached Obsidian with plugins ready, then timed out waiting for application window focus. Report: focused=true, active=false, activeDocumentUrl=about:blank, activePath=null, documentEditors=0. Failure PNG is an empty New tab (no property editor, so no clipping/focus-ring/selected-row/locked-row). Harness now destroys the leftover about:blank Electron window and clicks the tab strip; Athena xvfb-run starts xfwm4. Focused unit tests 8/8. Retrying Athena instead of closing.

[2026-11-23T16:18:41Z · bob-cli-pf.4.1.7.4--a] PROPOSED FOLLOW-UP: docs-check task-drawers.md missing from nav — npm run docs:check reports docs/develop/task-drawers.md is not listed in the docs nav. Pre-existing and already tracked as bob-cli-ph.1; this phase did not change docs nav.

[2026-11-23T16:18:57Z · bob-cli-pf.4.1.7.4--a] PROPOSED FOLLOW-UP: task_reqs README twin-copy drift — npm test reported the task_reqs plugin README and its twin copy have drifted. Pre-existing; unrelated to property-editor landing repairs.

[2026-11-23T16:19:04Z · bob-cli-pf.4.1.7.4--a] PROPOSED FOLLOW-UP: bob-cli-km/bob-cli-io isolation-pass timing flakes — npm test 9028 pass / 4 fail / 5 skip; the isolation-pass failures are on bob-cli-km and bob-cli-io. Pre-existing timing flakes; not caused by property-editor work.

[2026-11-23T16:19:22Z · bob-cli-pf.4.1.7.4--a] Athena monitor 7c632j PASS 129/129 (exit 0). Real-Obsidian Property Editor acceptance on project-note.md: write paths, panes, stale-draft keep, history reopen, YAML Done, close keys, unload, every entry point, and light/dark × wide/narrow screenshots. pluginReady active/navigation/commandMode/fixtureIndexed. coverage_fail 0. selectedDisplay flex; selectedDiffers true; focusOutlineWidth 2; lockedContrast 6.69 light / 8.13 dark; clipped/keyValueOverlap/rowOverlap/valueOverflow all false.

PNG review:
- wide-light: keys and values in columns; selected project_digest has light purple fill and a 2px purple focus ring; locked type muted and readable; heading PROJECT · PROPERTIES and footer fully visible; no clipping.
- wide-dark: same layout; selected row has dark purple fill and a 2px purple focus ring; locked type muted; no clipping.
- narrow-light: stacked key-above-value rows stay inside their buttons; values do not paint onto the next row; selected project_digest has purple fill and a 2px ring; locked type muted; heading and footer visible.
- narrow-dark: same stacked layout; selected fill and ring; locked type readable; no overflow.

Artifacts: report file:explicit:49ee66906e8ea8acb9a84f58; wide-light file:explicit:5920b45f8a4e4c729e2d738e; wide-dark file:explicit:bdd1744c20a50aa51751a550; narrow-light file:explicit:8168a7fbdad3b7c39330defb; narrow-dark file:explicit:848daf017651f258b7137e00; evidence zip file:explicit:36d3fab3790612136e5f0ca8. epic-symbols: none leftover.

## Dependencies

- **Depends on:** [bob-cli-pf.4.1.7.3](bob-cli-pf.4.1.7.3.md) ✓ · ⧖ 2026-11-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pf.4.1.7.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.4.1.7.4.md) | [bob-cli-pf.4.1.7.4](bob-cli-pf.4.1.7.4.md) | 9 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@1408a83`](https://github.com/bobs-org/bob-plugins/commit/1408a834014eb1dfb1f856f5f9c32f73356d07b3) | feat(property-editor): distinguish selected and locked rows | [bob-cli-pf.4.1.7.4](bob-cli-pf.4.1.7.4.md) | 2026-11-23 09:00:34 EST |
| bob-plugins | [`bob-plugins@e06f85e`](https://github.com/bobs-org/bob-plugins/commit/e06f85e3462eb76b494da2fcfcd5c143137a36d3) | fix(e2e): close Obsidian's blank startup window before Property Editor | [bob-cli-pf.4.1.7.4](bob-cli-pf.4.1.7.4.md) | 2026-11-23 09:25:53 EST |
| bob-plugins | [`bob-plugins@2a78691`](https://github.com/bobs-org/bob-plugins/commit/2a7869183f19a1d3cf6b6277688f8c84f4c51743) | fix(property-editor): keep requested edit key across empty cache | [bob-cli-pf.4.1.7.4](bob-cli-pf.4.1.7.4.md) | 2026-11-23 09:45:07 EST |
| bob-plugins | [`bob-plugins@337977b`](https://github.com/bobs-org/bob-plugins/commit/337977b0c6ab5d4dcb2fa206d1d8de0e75ef955a) | fix(e2e): match Property Editor stale-refusal copy | [bob-cli-pf.4.1.7.4](bob-cli-pf.4.1.7.4.md) | 2026-11-23 09:56:40 EST |
| bob-plugins | [`bob-plugins@b75ed48`](https://github.com/bobs-org/bob-plugins/commit/b75ed48930150fe5268283d3d92b0921187fa65d) | fix(e2e): match quoted YAML on Property Editor stale-refusal bytes | [bob-cli-pf.4.1.7.4](bob-cli-pf.4.1.7.4.md) | 2026-11-23 10:06:17 EST |
| bob-plugins | [`bob-plugins@074bf2d`](https://github.com/bobs-org/bob-plugins/commit/074bf2d3d71b4731e15738919e849c69e41c0ff9) | test(property-editor): wait for exact undo draft, not held-draft substring | [bob-cli-pf.4.1.7.4](bob-cli-pf.4.1.7.4.md) | 2026-11-23 10:16:58 EST |
| bob-plugins | [`bob-plugins@e60541b`](https://github.com/bobs-org/bob-plugins/commit/e60541b3ec35b6d9b5aef8b886ce3e57a473f77e) | fix(property-editor): stack narrow rows on an inner grid | [bob-cli-pf.4.1.7.4](bob-cli-pf.4.1.7.4.md) | 2026-11-23 10:32:00 EST |
| bob-plugins | [`bob-plugins@e2e944a`](https://github.com/bobs-org/bob-plugins/commit/e2e944af199ed8d49685f0b7616fc10fcc73e009) | fix(property-editor): restore selected-row fill over the button reset | [bob-cli-pf.4.1.7.4](bob-cli-pf.4.1.7.4.md) | 2026-11-23 10:44:09 EST |
| bob-plugins | [`bob-plugins@2661302`](https://github.com/bobs-org/bob-plugins/commit/2661302799f3dc4842ca4782a21221201d32673b) | fix(property-editor): grow stacked rows with a flex button | [bob-cli-pf.4.1.7.4](bob-cli-pf.4.1.7.4.md) | 2026-11-23 10:56:03 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pf.4.1.7.4--2][1] | Diagnose Athena Property Editor e2e focus timeout before fixing harness | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.4.1.7.4.md

<!-- sase:referenced-by:end -->
