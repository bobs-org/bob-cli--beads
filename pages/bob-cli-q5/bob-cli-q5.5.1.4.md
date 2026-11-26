# Bead: bob-cli-q5.5.1.4 — Snoozed rows and heading summaries

[Bead Pages](../README.md) / [bob-cli-q5.5.1](bob-cli-q5.5.1.md) / bob-cli-q5.5.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.5.md) · **Assignee:** `bob-cli-q5.5.1.4` · **Size:** medium
**Created:** 2026-11-26 15:37:08 EST · **Closed:** 2026-11-26 18:35:58 EST
**Plan:** [202611/snooze\_display\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/snooze_display_marks.md)

## Description

snoozed-row-paint: paint active, due, blocked, ignored, and struck Snoozed rows plus heading summaries in Live Preview and Reading view.

## Notes

[2026-11-26T23:35:47Z · bob-cli-q5.5.1.4] PROPOSED FOLLOW-UP: bob-plugins docs:check fails on upstream bob-cli vault-format.md word budget (6030 words, cap 6000 for reference/) — pre-existing on origin/master, unrelated to row-paint files; triage as task bead if not already tracked

[2026-11-26T23:35:58Z · bob-cli-q5.5.1.4] Implemented snoozed-row-paint: pure SM-R model (143b: paint + heading summary, all 18 vectors verbatim), Live Preview (278a) and Reading (278b) paint with structural-H2, fence/indent/duplicate-header, historical, and toggle guards, shared snooze refresh lifecycle, styles, and test-ledger-tools-snooze-row-paint (11 tests). Updated definition toggle test 2->3 extensions. Verified: 42/42 snooze display tests, 43/43 snooze model vectors, 46/46 board+stats stylesheet, full test:unit 10118 pass 0 fail 4 skipped; build:check and validate green; deployed bob-ledger-tools (main.js + styles.css) via bob plugins sync from linked checkout. docs:check lint failure on upstream vault-format.md budget recorded as PROPOSED FOLLOW-UP.

## Dependencies

- **Depends on:** [bob-cli-q5.5.1.3](bob-cli-q5.5.1.3.md) ✓ · ⧖ 2026-11-26
- **Blocks:** [bob-cli-q5.5.1.5](bob-cli-q5.5.1.5.md) ◐ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.5.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.5.1.4/README.md) | [bob-cli-q5.5.1.4](bob-cli-q5.5.1.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@514f799`](https://github.com/bobs-org/bob-plugins/commit/514f7992af9ff5a6fa754a24d95687bcf4b144b2) | feat(snooze): paint Snoozed rows and heading summaries | [bob-cli-q5.5.1.4](bob-cli-q5.5.1.4.md) | 2026-11-26 18:36:55 EST |
