# Bead: bob-cli-pl.7 — Hue, default type, and clock-policy stages (bob-plugins)

[Bead Pages](../README.md) / [bob-cli-pl](README.md) / bob-cli-pl.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5y.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5y.linker.w1.md) · **Assignee:** `bob-cli-pl.7` · **Size:** medium
**Created:** 2026-11-22 20:56:40 EST · **Closed:** 2026-11-25 19:19:13 EST
**Plan:** [202611/area\_project\_cards.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/area_project_cards.md)

## Description

editor-policy-stages: add the swatch stage with a live tint preview, the type picker with legacy theme migration, and the four-mode clock-policy stage with shadowed-pair cleanup.

## Notes

[2026-11-26T00:17:37Z · bob-cli-pl.7] PROPOSED FOLLOW-UP: Fix the stale date expectation in scripts/test-task-status-cycler-open-line.cjs — on 2026-11-26 its dynamic NEW_TASK is created::2026-11-26 while two assertions still expect 2026-11-25; the test and cycler sources are unchanged from HEAD, and no matching bead was found.

[2026-11-26T00:17:38Z · bob-cli-pl.7] PROPOSED FOLLOW-UP: Run the live Property Editor policy-stage acceptance and capture screenshots — exact command: xvfb-run -a node scripts/obsidian-property-editor-e2e.cjs --executable /snap/bin/obsidian --out /tmp/bob-cli-pl7-policy-shots --report /tmp/bob-cli-pl7-policy-e2e.json; verdict here: unrun because this host has neither /snap/bin/obsidian nor xvfb-run. Offline e2e passed.

[2026-11-26T00:19:13Z · bob-cli-pl.7] Implemented and built hue, default-type, and clock-policy stages with live preview, legacy theme migration, shadowed-clock cleanup, fixtures, offline acceptance coverage, docs, and UI styles. npm test ran: 9698 pass; 2 unchanged cycler date assertions fail on Nov 26, and the untouched frees-marks CPU test exceeded budget once in-suite but passed standalone; all 26 perf tests pass. bob-ledger-tools sync dry-run is up to date. Live Obsidian screenshots are proposed follow-up because this host lacks Obsidian and xvfb-run. Epic symbols: none.

## Dependencies

- **Depends on:** [bob-cli-pl.6](bob-cli-pl.6.md) ✓ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-pl.9](bob-cli-pl.9.md) ◐ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pl.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pl.7/README.md) | [bob-cli-pl.7](bob-cli-pl.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@691182f`](https://github.com/bobs-org/bob-plugins/commit/691182f43befa4f2b0c980340e6f2dbd7796b0f3) | feat(property-editor): add hue type and clock policy stages | [bob-cli-pl.7](bob-cli-pl.7.md) | 2026-11-25 19:35:59 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pl.7][1] | Verify recorded follow-up notes and closeout evidence | 3 |
| read-by | [agent:fx][2] | Map the pl epic dependency graph | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pl.7/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.fx/README.md

<!-- sase:referenced-by:end -->
