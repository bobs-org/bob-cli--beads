# Bead: bob-cli-q4.8.1.3 — Publish taskSettle v1 with the pending scheduler

[Bead Pages](../README.md) / [bob-cli-q4.8.1](bob-cli-q4.8.1.md) / bob-cli-q4.8.1.3

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q4.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q4.8.md) · **Assignee:** `bob-cli-q4.8.1.3` · **Size:** medium
**Created:** 2026-11-25 10:27:09 EST
**Plan:** [202611/task\_settle\_twin.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_settle_twin.md)

## Description

pending-api: implement the shared 500 ms pending scheduler, early flush and teardown lifecycle, publish the complete taskSettle v1 namespace, document its consumer contract, verify skew and race behavior, and deploy bob-ledger-tools.

## Notes

[2026-11-25T17:55:05Z · bob-cli-q4.8.1.3--1] PROPOSED FOLLOW-UP: Reduce docs word-budget overages — docs:check fails on clean plugin base fdde3dcf against Bob CLI docs 0742684 with plugin-apis at 9287/8000 words and navigation-hotkeys at 6068/6000; current source is 9961/8000 and 6068/6000. The base run confirms both over-budget failures predate this phase.

## Dependencies

- **Depends on:** [bob-cli-q4.8.1.2](bob-cli-q4.8.1.2.md) ✓ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q4.8.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q4.8.1.3.md) | [bob-cli-q4.8.1.3](bob-cli-q4.8.1.3.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@c945420`](https://github.com/bobs-org/bob-plugins/commit/c9454208ac8eede09f338c328ab640166ea3168e) | feat(ledger-tools): publish task settle v1 scheduler | [bob-cli-q4.8.1.3](bob-cli-q4.8.1.3.md) | 2026-11-25 12:35:32 EST |
| bob-plugins | [`bob-plugins@abbac5a`](https://github.com/bobs-org/bob-plugins/commit/abbac5acc380b651c091657d40f77d43680a9054) | test(ledger-tools): measure resident count cpu time | [bob-cli-q4.8.1.3](bob-cli-q4.8.1.3.md) | 2026-11-25 13:25:22 EST |
