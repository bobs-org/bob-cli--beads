# Bead: bob-cli-rv.8 — Bob Mac Capture re-syncs fixtures and pins minute recall ages

[Bead Pages](../README.md) / [bob-cli-rv](README.md) / bob-cli-rv.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1ho](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1ho.md) · **Assignee:** `bob-cli-rv.8` · **Size:** small
**Created:** 2026-11-28 08:22:27 EST · **Closed:** 2026-11-28 10:18:16 EST
**Plan:** [202611/task\_log\_datetime\_stamps.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_log_datetime_stamps.md)

## Description

mac: re-copy the regenerated req_close vectors, add tests that a minute Cancel `last_used` renders a minute age, and refresh the stale day-only comments.

## Notes

[2026-11-28T15:18:16Z · bob-cli-rv.8] Re-copied tests/fixtures/req_close/vectors.json from bob-cli into bob-mac-capture Tests/Fixtures/req_close/vectors.json and confirmed with cmp (24 stamped write cases). log-recall-vectors.json already matched bob-cli. Kept the last_used ':' heuristic, refreshed day-only comments in LogRecallBandPresentation and CapturePomodoroClosePresentation, and added LogRecallStateTests for Cancel last_used 2026-11-28 14:32 (15m/2h), 2026-10-25 (Oct 25), and direct minuteAge (now/15m/2h/yesterday). just portable-check: 2928 tests, 0 failures, including the new LogRecallStateTests. No leftover --epic-symbol entries. Docs unchanged.

## Dependencies

- **Depends on:** [bob-cli-rv.1](bob-cli-rv.1.md) ✓ · ⧖ 2026-11-28
- **Depends on:** [bob-cli-rv.3](bob-cli-rv.3.md) ✓ · ⧖ 2026-11-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-rv.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-rv.8.md) | [bob-cli-rv.8](bob-cli-rv.8.md) | 0 |
