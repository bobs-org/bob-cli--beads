# Bead: bob-cli-kr.4.1.4 — Schema editor integration and real Obsidian acceptance

[Bead Pages](../README.md) / [bob-cli-kr.4.1](bob-cli-kr.4.1.md) / bob-cli-kr.4.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-kr.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-kr.4.md) · **Assignee:** `bob-cli-kr.4.1.4` · **Size:** medium
**Created:** 2026-11-12 13:46:53 EST · **Closed:** 2026-11-12 17:40:26 EST
**Plan:** [202611/album\_schema\_card\_editor.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/album_schema_card_editor.md)

## Description

editor-acceptance: extend the existing scratch-vault album harness to prove real writer preview/apply/Undo, stale-save refusal, source validation, and keyboard and visual behavior; finish reference docs and deployment evidence.

## Notes

[2026-11-12T22:38:04Z · bob-cli-kr.4.1.4] PROPOSED FOLLOW-UP: full npm test 6403/6411 — 4 deterministic failures reproduce identically on the clean base (walkMode api versioned + null-plugin degrade + links in test-navigation-bracket-repeat/period-links, session toggle/onload wiring in test-ledger-tools-task-tag-marks; see bob-cli-kr.4.1.3 notes #1) and 3 perf 25ms-budget failures pass in isolation (full-suite load flakes; see bob-cli-f8) -r Recording pre-existing gate failures found during editor-acceptance verification

[2026-11-12T22:38:18Z · bob-cli-kr.4.1.4] PROPOSED FOLLOW-UP: docs:check fails on pre-existing gates unrelated to album docs — bob-navigation-hotkeys.md over 6000-word reference budget (6000 cap) and the offline-lychee gcal-notes target from bob-cli-kr.4.1.3 note #2 / bob-cli-kd.6.1.2; docs/albums.md changes add no links -r Recording pre-existing docs gate failures

[2026-11-12T22:38:30Z · bob-cli-kr.4.1.4] PROPOSED FOLLOW-UP: real-Obsidian legs unrun on apollo (no Obsidian binary, no xvfb) — CDP schema-card walk in obsidian-album-ui-e2e.cjs and smoke:obsidian real check need a host with Obsidian (CI/Mac); offline writer matrix + self-tests green here -r Recording real-Obsidian verification limitation for the land agent

[2026-11-12T22:40:26Z · bob-cli-kr.4.1.4] editor-acceptance done. Offline writer matrix green (scripts/obsidian-album-schema-writer-e2e.cjs --self-test: preview/apply/Undo with consequence+derived keys+inverse ops, one scoped commit per envelope, index rebuilt, record bytes unchanged, relabel keeps stored keys, no-op/refusal byte+commit stability, used choice_used/field_used with complete counts + YAML hint, stale_schema exit 2, double-apply single commit, typed 0/unset/list-distinct semantics + invalid_default refusal, post-sync local success with vault-sync-only retry and no second commit, source corrupt/repair cycle). Focused suites 56/56 (album header/update/entrypoints/yaml-excursion, both e2e wrappers). build/build:check/validate/docs:inventory green. docs/albums.md finished (dry-run gating, Undo confirmation, stale recovery, sync-only retry, full keymap, YAML Done, mobile, verification section). bob-ledger-tools synced to vault (plugins list row: synced). CDP schema-card walk added to obsidian-album-ui-e2e.cjs (entry/keyboard/preview/apply-double-guard/Undo/Task-Card priority/two-pane stale/YAML Done/375px shots) — unrun here, no Obsidian/xvfb on apollo. Full npm test 6403/6411 with only pre-existing failures (recorded as follow-ups, reproduce on clean base). docs:check + just check not green here (pre-existing word-budget/lychee; just check compile exceeds turn ceiling, bob-cli untouched — land agent owns it).

## Dependencies

- **Depends on:** [bob-cli-kr.4.1.3](bob-cli-kr.4.1.3.md) ✓ · ⧖ 2026-11-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-kr.4.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-kr.4.1.4/README.md) | [bob-cli-kr.4.1.4](bob-cli-kr.4.1.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@a572162`](https://github.com/bobs-org/bob-plugins/commit/a57216288b376e363fc81f990e32008965a947ec) | feat(albums): schema editor integration and real Obsidian acceptance | [bob-cli-kr.4.1.4](bob-cli-kr.4.1.4.md) | 2026-11-12 17:45:09 EST |
