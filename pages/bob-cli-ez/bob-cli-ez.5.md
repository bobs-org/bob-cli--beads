# Bead: bob-cli-ez.5 — Ledger-tools Keep inbox status-bar item

[Bead Pages](../README.md) / [bob-cli-ez](README.md) / bob-cli-ez.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2y.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2y.linker.w0.md) · **Assignee:** `bob-cli-ez.5` · **Size:** medium
**Created:** 2026-10-31 13:32:41 EDT · **Closed:** 2026-10-31 15:59:28 EDT
**Plan:** [202610/gkeep\_footer\_indicator.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/gkeep_footer_indicator.md)

## Description

keep-indicator-view: add the bob-keep-inbox status-bar item to bob-ledger-tools with a pure view model, the live Tasks-cache inbox count, cache-only Keep reads, the full visual design, the inbox click, tests, and docs.

## Notes

[2026-10-31T19:58:51Z · bob-cli-ez.5] PROPOSED FOLLOW-UP: add a decisions-web record that bob owns the Keep count, its cache, and its check budget (epic plan keep-indicator-actions step 10; decision_record=no for this phase, so skipped here)

[2026-10-31T19:59:05Z · bob-cli-ez.5] PROPOSED FOLLOW-UP: fix two pre-existing bob-plugins test failures that reproduce identically on the clean base tree (verified via git stash): test-ledger-tools-note-ready "the startup storm is linear" (expects 2 scans, gets 1) and test-ledger-tools-relation-index "registers after layout-ready" (scan never finishes); unrelated to keep-indicator-view

[2026-10-31T19:59:28Z · bob-cli-ez.5] keep-indicator-view done in bob-plugins 91ae2f8: pure keepInboxViewModel/decode/count, render + KeepInbox mixin wired after the review footer, cache-only gkeep status reads, Tasks-cache inbox count, inbox click, styles, docs; 11/11 new tests pass, build:check + docs gates pass; 2 unrelated failures (note-ready, relation-index) reproduce on clean base and are filed as follow-ups

## Dependencies

- **Depends on:** [bob-cli-ez.3](bob-cli-ez.3.md) ✓ · ⧖ 2026-10-31
- **Blocks:** [bob-cli-ez.6](bob-cli-ez.6.md) ◐ · ⧖ 2026-10-31

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ez.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ez.5/README.md) | [bob-cli-ez.5](bob-cli-ez.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@38b9114`](https://github.com/bobs-org/bob-plugins/commit/38b91140a987e1a8c99d015944f5dcc176a726bc) | feat(ledger-tools): add the Keep inbox status-bar item | [bob-cli-ez.5](bob-cli-ez.5.md) | 2026-10-31 16:01:21 EDT |
