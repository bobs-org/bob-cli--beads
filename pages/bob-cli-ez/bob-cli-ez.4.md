# Bead: bob-cli-ez.4 — Command Mode preview API

[Bead Pages](../README.md) / [bob-cli-ez](README.md) / bob-cli-ez.4

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2y.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2y.linker.w0.md) · **Assignee:** `bob-cli-ez.4` · **Size:** small
**Created:** 2026-10-31 13:32:41 EDT
**Plan:** [202610/gkeep\_footer\_indicator.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/gkeep_footer_indicator.md)

## Description

command-mode-preview-api: add `api.commandMode.preview(argv)` to bob-command-mode so a sibling plugin can open the sheet straight into a row's preview stage, with tests and docs.

## Notes

[2026-10-31T17:47:26Z · bob-cli-ez.4] PROPOSED FOLLOW-UP: bob-plugins npm test has 5 failures that reproduce on the clean base (production sheet render and clicks use real DOM APIs; ledger-tools relation-index/startup-storm/reload-event/create-listener tests)

[2026-10-31T17:47:38Z · bob-cli-ez.4] PROPOSED FOLLOW-UP: decision_record=no, so the decisions-web record (bob owns the Keep count, cache, and check budget) was skipped per the epic DECISIONS

## Dependencies

- **Blocks:** [bob-cli-ez.6](bob-cli-ez.6.md) ◐ · ⧖ 2026-10-31

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ez.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ez.4/README.md) | [bob-cli-ez.4](bob-cli-ez.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@b0db27a`](https://github.com/bobs-org/bob-plugins/commit/b0db27a60f92dca1f1769de7d510986a173e84d2) | feat(command-mode): add api.commandMode.preview | [bob-cli-ez.4](bob-cli-ez.4.md) | 2026-10-31 13:47:55 EDT |
