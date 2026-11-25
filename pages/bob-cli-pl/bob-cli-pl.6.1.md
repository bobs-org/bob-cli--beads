# Bead: bob-cli-pl.6.1 — Area and project settings in the Property Editor

[Bead Pages](../README.md) / [bob-cli-pl.6](bob-cli-pl.6.md) / bob-cli-pl.6.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pl.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pl.6.md) · **Assignee:** `bob-cli-pl.6.1.land`
**Created:** 2026-11-24 15:49:21 EST · **Closed:** 2026-11-25 18:10:15 EST
**Plan:** [202611/area\_project\_settings.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/area_project_settings.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/area_project_settings.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/area_project_settings.md

<!-- sase:links:end -->

## Description

Complete bob-cli-pl.6 with contract-driven settings, safe set and clear actions, project task handoffs, and verified entry points in the existing Property Editor.

## Notes

[2026-11-25T03:26:23Z · bob-cli-pw.5.1.land] DISCOVERED ISSUE: Landing bob-cli-pw.5.1 triage of phase bob-cli-pw.5.1.4 note #1 independently measured docs/reference/json-outputs.md with bob_docs.markdown.count_words: 447ef1a5^ = 6000, 447ef1a5 = 6005. Phase bob-cli-pl.6.1.1 settings-contract row added the 5 words crossing the 6000 cap. Current meeting CLI e4c96b05 adds another 25 (6030). No duplicate task after all-status search and last-week CI sweep. The meeting landing repair tale will trim the shared page below the cap while preserving both contracts, so do not duplicate that edit; this note records causal ownership and planned integration.

[2026-11-25T23:10:15Z · bob-cli-pl.6.1.land] LANDED. Verified: all 5 phases closed and their notes addressed. bob-cli 447ef1a5 (6.1.1) returns view.report.contract in successful props update JSON (preview/apply/no-op/restore; ordinary notes omit it); cargo test --test cli props 29/29 at 9dd67c62; no later bob-cli commit touches props. bob-plugins d55a1759..9d305022: 298w settings rows/groups/capability fallback, 298x/298y typed setting.set/clear stages (summary N/140, ready cap 1-999|off, review 1-365, capture names list, stats-root toggle, temporary generic parent/color/type/clock), 298z area/project == registry after bank/album/record with bank precedence and teardown, setting/focusSettings requests incl. ghosts and theme/offclock aliases, ^prj Goal/Starts/Depends-on/status handoff with exact line-text validation and cursor fallback, no writes on open/paint/navigation. All fragments <=1000 lines (298f 977). Real-Obsidian acceptance 363/363 + 70/70 coverage recorded on 6.1.5. Decisions honored: card_structure_counts=no; no memory edits. INTEGRATION: reviewed 41 non-epic bob-plugins commits since d55a1759 and 27 bob-cli commits since 447ef1a5. a71a59db area/project _ folds and the foot editor hook still route through homeCardOpenSetting -> setting/focusSettings; cf8722f1 soft-line summary already lands in 298y; 1ff10aa4/fbe5fd86/7d53d189 bank fold/title keep == bank precedence. Focused suites on aecff7d2: settings-rows 21, setting-actions 18, settings-entrypoints 21, stages 10, schema-double-equals 42, home-card-host 17, plus 12 other property-editor suites, all green. LANDING FIX (epic-caused, from 6.1.5 note #8): generic setting stages (Capture names) now paint setting notes above preview and Save/Cancel; Review shows its residence scope once (preview text no longer repeats it, Bob's matching effect deduped against the help line). Two regression tests fail on the old code. Full npm test 9685 pass/0 fail/5 skipped + perf 26/26, validate 12/12, build:check clean. bob plugins sync -p bob-ledger-tools deployed to apollo, vault main.js byte-identical. Not rerun in real Obsidian; the e2e Review-scope check still matches the retained help line. FOLLOW-UPS: docs budgets -> +1 bob-cli-il (bob-ledger-tools.md 6040) and +1 bob-cli-ob (bob-navigation-hotkeys.md 6068, plugin-apis.md 9279 warning). capture-syntax.md 6058 (6.1.5 #7) and json-outputs.md 6007 (epic note #1) were re-crossed by bob-cli-q7.1 4d930129 after earlier trims, so recorded as DISCOVERED ISSUE on active epic bob-cli-q7, not this epic. Mac keyboard/protocol budgets no longer fail: declined. Load timing flakes (bob-cli-km/pg/f8) and the bob-cli-n0 album held-lock failure are already tracked and did not reproduce in this landing's green full run: declined, no +1. Stale nav-hotkeys main.js (6.1.5 #10, bob-cli-q4.10.1) is now build:check clean: declined. epic-symbols: none. SEAM for pl.7/.8: propertyEditorRegisterSettingStageHandler(id, handler) replaces one setting's handler; propertyEditorResolveSettingStage(entry) dispatch returns {ok, stage?, toggle?, message?}; openPropertyEditor({filePath, setting|focusSettings}); documented in docs/develop/architecture.md.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pl.6.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pl.6.1.land/README.md) | [bob-cli-pl.6.1](bob-cli-pl.6.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@ea3bc6a`](https://github.com/bobs-org/bob-plugins/commit/ea3bc6a42500cb93ea77f69f4e50fbd7adf44261) | fix(property-editor): keep setting notes above Save/Cancel and show Review scope once | [bob-cli-pl.6.1](bob-cli-pl.6.1.md) | 2026-11-25 18:11:31 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pl.6.1.3][1] | Need parent epic DECISIONS and phase notes for setting-actions | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pl.6.1.3/README.md

<!-- sase:referenced-by:end -->
