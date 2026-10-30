# Bead: bob-cli-es.2 — Bob Ledger Tools paints the stamp as a live health line

[Bead Pages](../README.md) / [bob-cli-es](README.md) / bob-cli-es.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bh](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bh.md) · **Assignee:** `bob-cli-es.2` · **Size:** small
**Created:** 2026-10-30 18:30:34 EDT · **Closed:** 2026-10-30 19:49:36 EDT
**Plan:** [202610/gcal\_events\_sync\_stamp.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/gcal_events_sync_stamp.md)

## Description

plugin-paint: in bob-plugins, recognize the stamp in Live Preview and Reading view, paint it as a muted caption, mark it stale on today's note, refresh it each minute, then test, document, and run `bob plugins sync`.

## Notes

[2026-10-30T23:49:18Z · bob-cli-es.2] PROPOSED FOLLOW-UP: bob-plugins npm test still red on the two layout-ready harness failures tracked by bob-cli-eh (note-ready startup storm 1!==2; relationIndex layout-ready waitUntil) — reproduced on this tree and on a clean stash of origin/master; not caused by stamp painting. The keystroke-rank 12ms budget also flaked under load (14ms) and passed on the clean tree.

[2026-10-30T23:49:36Z · bob-cli-es.2] Ledger Tools paints the Events stamp in Live Preview and Reading view as a muted caption. Scan recognizes the CLI grammar (same-day and dated ↻ lines, skips lists/fences/outside Events) without changing row scan. stamp_refresh=on_change: GCAL_EVENTS_STAMP_STALE_AFTER_MINUTES is null and gcalEventsStampState stays fresh for old, future, and dated stamps. npm run build, focused gcal-events tests (8/8), and npm run docs:check passed. npm test 4538/4541 with the two bob-cli-eh layout-ready failures on clean master plus a keystroke-rank flake. Deployed bob-ledger-tools via bob plugins sync --repo this checkout -p bob-ledger-tools -F.

## Dependencies

- **Depends on:** [bob-cli-es.1](bob-cli-es.1.md) ✓ · ⧖ 2026-10-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-es.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-es.2/README.md) | [bob-cli-es.2](bob-cli-es.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@4e31220`](https://github.com/bobs-org/bob-plugins/commit/4e3122080f6b1c1f9413b29c63e4df50373eef90) | feat(ledger-tools): paint the Events sync stamp as a muted caption | [bob-cli-es.2](bob-cli-es.2.md) | 2026-10-30 19:50:39 EDT |
