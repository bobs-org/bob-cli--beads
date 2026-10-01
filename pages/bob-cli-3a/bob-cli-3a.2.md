# Bead: bob-cli-3a.2 — Live Preview decoration and rendered-view marks

[Bead Pages](../README.md) / [bob-cli-3a](README.md) / bob-cli-3a.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.3y](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.3y.md) · **Assignee:** `bob-cli-3a.2` · **Size:** medium
**Created:** 2026-10-01 11:19:39 EDT · **Closed:** 2026-10-01 12:01:06 EDT
**Plan:** [202610/fresh\_mark.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/fresh_mark.md)

## Description

mark-surfaces: wire the model into Obsidian. Add a Prec.highest CodeMirror ViewPlugin that replaces canonical stamps in Live Preview, with reveal-on-cursor and click-to-reveal. Add a markdown post-processor for reading view and Tasks query results, a filesystem-free cached mark snapshot refreshed on the status bar paths, a session toggle command, and the repair flag on leftover Dataview pills, all with stubbed CodeMirror tests.

## Notes

[2026-10-01T16:01:06Z · bob-cli-3a.2] mark-surfaces done: Live Preview ViewPlugin (Prec.highest, reveal-on-cursor, click-to-reveal, code skips), rendered-view post-processor at sortOrder 50, filesystem-free snapshot with 150ms refresh on all status-bar paths, session toggle + bob-fresh-marks body class, repair-flag CSS; new surfaces test file 13 tests pass; full bob-plugins suite 1066 pass, validate 6/6, bob plugins sync ok (2 copied)

## Dependencies

- **Depends on:** [bob-cli-3a.1](bob-cli-3a.1.md) ✓ · ⧖ 2026-10-01
- **Blocks:** [bob-cli-3a.3](bob-cli-3a.3.md) ◐ · ⧖ 2026-10-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-3a.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-3a.2/README.md) | [bob-cli-3a.2](bob-cli-3a.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@2b128b7`](https://github.com/bobs-org/bob-plugins/commit/2b128b71465f6d4ec0cc71826e6d52e3b95c9e91) | feat(ledger-tools): Live Preview decoration and rendered-view freshness marks | [bob-cli-3a.2](bob-cli-3a.2.md) | 2026-10-01 12:03:42 EDT |
