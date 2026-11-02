# Bead: bob-cli-fl.4 — bob-cli: bob task reconcile settles ended off-clock Event Tasks

[Bead Pages](../README.md) / [bob-cli-fl](README.md) / bob-cli-fl.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2z.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2z.linker.w0.md) · **Assignee:** `bob-cli-fl.4` · **Size:** medium
**Created:** 2026-11-01 21:46:35 EST · **Closed:** 2026-11-02 02:15:24 EST
**Plan:** [202611/off\_clock\_pomodoros.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/off_clock_pomodoros.md)

## Description

settle-ended-events: reconcile turns ended #offclock Event Tasks still parked under an unstarted placeholder into closed [off:: Nm] MEETs trimmed around on-clock sessions, plus its decision record.

## Notes

[2026-11-02T07:15:24Z · bob-cli-fl.4] Settle landed: reconcile turns ended #offclock Event Tasks under open () placeholders into closed [off::] MEETs trimmed around on-clock sessions, completes rows with [x]+completion date. Verified: 6 new CLI settle tests pass, all 173 task_status_hooks CLI tests pass, 123 lib hook tests pass, fmt/clippy clean for settle, docs-gen+docs-check pass. Human prints '◌ settled {title} {span} off the clock', JSON adds settled[]; docs and glossary sentence updated.

## Dependencies

- **Depends on:** [bob-cli-fl.1](bob-cli-fl.1.md) ✓ · ⧖ 2026-11-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-fl.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fl.4/README.md) | [bob-cli-fl.4](bob-cli-fl.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f171e3c`](https://github.com/bobs-org/bob-cli/commit/f171e3cc2096ce3e6f3658e550ff3d22b7d5fd84) | feat(task-status-hooks): settle ended off-clock event tasks into closed sessions | [bob-cli-fl.4](bob-cli-fl.4.md) | 2026-11-02 02:17:13 EST |
