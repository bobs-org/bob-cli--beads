# Bead: bob-cli-ij.2 — bob-plugins mirrors and grey root lanes

[Bead Pages](../README.md) / [bob-cli-ij](README.md) / bob-cli-ij.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.19s](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.19s.md) · **Assignee:** `bob-cli-ij.2` · **Size:** medium
**Created:** 2026-11-07 17:26:28 EST · **Closed:** 2026-11-07 18:33:50 EST
**Plan:** [202611/gtd\_root\_and\_area\_colors.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gtd_root_and_area_colors.md)

## Description

plugins: in bob-plugins, mirror nearest-note colors and the grey mute in the home-chip and type-hue mirrors, keep muted roots gray in every root lane, copy the shared vectors byte for byte, then test, build, and run `bob plugins sync`.

## Notes

[2026-11-07T23:33:36Z · bob-cli-ij.2] PROPOSED FOLLOW-UP: Trim or split bob-plugins docs/bob-ledger-tools.md — it sat at exactly the 6000-word reference/ budget before this phase and is now 5999/6000 (bob-docs count_words), so any further addition fails `npm run docs:check`; this phase had to trim three redundant phrases to land its grey-root/grey-type wording.

[2026-11-07T23:33:50Z · bob-cli-ij.2] plugins phase done in bob-plugins (bob-ledger-tools). Vectors: copied bob-cli master pomodoro_homes + pomodoro_themes vectors over all 3 bob-plugins copies; cmp identical. Home mirror: new 142a-pomodoro-home-colors.js (R8 nearest area/project color: walk; grey/gray -> hue null + hue_source muted; invalid/list values lint area_color_invalid once per path across the walked chain and inherit; else top-area hash) replaces pomodoroHomeHueForArea; pomodoroHomeResolve returns hue_source + root_hue; root groups, chip lead hue, Today roots, and root marks wear the root's own hue (grey root stays null/gray). Type mirror: pomodoroThemesAreasMap records grey top-level areas as null; pomodoroThemeResolveHue returns {hue:null,hue_source:area}; new pomodoroThemeHueIsMuted makes pills (LP + reading), task-type #TYPE identity, and plan pills render it muted like exempt; Stats type lane already grays null hues. Strips: statsPanelDistinctHues sets hue_source muted roots gray up front (never claims/shades); Day strip, Stats window lanes, Stats root rows, and period lane + parts row follow; muted roots sort after coloured, before buckets. Tests: new nearest-color-and-grey + area-grey-mutes vectors pass; added muted-root tests to day-strip-lanes (new mutedRoots fixture), stats-lanes, period-strip (verified they fail with the fix reverted), plus R8 resolve/root-mark, Today-roots root_hue, grey-area type pill/area-map/statsThemeRef, and task-type identity tests. Docs: docs/bob-ledger-tools.md updated word-neutrally (page budget 6000; now 5999). Gates: npm run build, npm test (5686/5686 pass), npm run validate (9/9), npm run docs:check all pass. Deployed with bob plugins sync -p bob-ledger-tools -F from this checkout (forced only because the vault deploy was another checkout's dirty build that I verified byte-identical to master 9dd2888 for manifest/main.js/styles.css); vault main.js matches the build. bob-plugins changes are uncommitted pending the finalizer commit.

## Dependencies

- **Depends on:** [bob-cli-ij.1](bob-cli-ij.1.md) ✓ · ⧖ 2026-11-07
- **Blocks:** [bob-cli-ij.3](bob-cli-ij.3.md) ◐ · ⧖ 2026-11-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ij.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ij.2/README.md) | [bob-cli-ij.2](bob-cli-ij.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@59df267`](https://github.com/bobs-org/bob-plugins/commit/59df26757cecfcec89bd3c4f07eeed0b2114e912) | feat(ledger-tools): mirror nearest-note area/project colors and keep grey roots gray | [bob-cli-ij.2](bob-cli-ij.2.md) | 2026-11-07 18:34:27 EST |
