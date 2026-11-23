# Bead: bob-cli-pf.4.1.6 — Real Obsidian acceptance and editor documentation

[Bead Pages](../README.md) / [bob-cli-pf.4.1](bob-cli-pf.4.1.md) / bob-cli-pf.4.1.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pf.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.4.md) · **Assignee:** `bob-cli-pf.4.1.6` · **Size:** medium
**Created:** 2026-11-22 23:01:42 EST · **Closed:** 2026-11-23 02:51:21 EST
**Plan:** [202611/property\_editor\_core.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/property_editor_core.md)

## Description

acceptance-docs: add real-Obsidian acceptance and offline self-tests, document the core editor, and record verified evidence for closing bob-cli-pf.4.

## Notes

[2026-11-23T07:51:21Z · bob-cli-pf.4.1.6--1] Acceptance and docs work is landed in bob-plugins commit c60b2d3e. Verified: Property Editor focused suite 56/56 (including offline acceptance self-test); npm run build unchanged; npm run validate 12/12 plugins; prior npm run docs:check passed 447 tests with one optional font-asset skip; bob plugins sync copied bob-ledger-tools and bob-command-mode; no epic symbols remain. Full npm test exited 1 on three performance thresholds (event-link 39.1/25 ms, free-marks 198/25 ms, taskLinks p95 12.21/12 ms); each exact case passed when rerun alone. Real Obsidian Electron acceptance could not run because the Electron executable is unavailable; bob CLI 0.6.0 is installed.

## Dependencies

- **Depends on:** [bob-cli-pf.4.1.5](bob-cli-pf.4.1.5.md) ✓ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pf.4.1.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.4.1.6.md) | [bob-cli-pf.4.1.6](bob-cli-pf.4.1.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@c60b2d3`](https://github.com/bobs-org/bob-plugins/commit/c60b2d3ead07c8fa008892401e689a27d5c5a293) | feat(property-editor): add Obsidian acceptance workflow and docs | [bob-cli-pf.4.1.6](bob-cli-pf.4.1.6.md) | 2026-11-23 02:38:40 EST |
