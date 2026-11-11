# Bead: bob-cli-kf.5 — Subprocess reaper and notify hardening

[Bead Pages](../README.md) / [bob-cli-kf](README.md) / bob-cli-kf.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1bj](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1bj.md) · **Assignee:** `bob-cli-kf.5` · **Size:** small
**Created:** 2026-11-11 13:33:44 EST · **Closed:** 2026-11-11 14:09:31 EST
**Plan:** [202611/security\_audit\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/security_audit_fixes.md)

## Description

subprocess-hardening: bound the post-exit pipe-drain phase with a deadline, fix the straggler-kill PID-reuse ordering, and reject huge sleep values that panic Duration::from_secs_f64 in bob pomodoro notify.

## Notes

[2026-11-11T19:09:31Z · bob-cli-kf.5] Implemented bounded post-exit draining and incomplete-output reporting for subprocess pipes, killed process groups before reaping leaders, and rejected notify sleeps above one year. Verified subprocess/notify tests and just lint.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kf.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kf.5/README.md) | [bob-cli-kf.5](bob-cli-kf.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`7b3f351`](https://github.com/bobs-org/bob-cli/commit/7b3f3512204e3c8fd394597d50d4491879e29f03) | fix(subprocess): bound pipe draining and harden notify sleeps | [bob-cli-kf.5](bob-cli-kf.5.md) | 2026-11-11 14:10:33 EST |
