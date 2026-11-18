# Bead: bob-cli-nb.5 — Mac cron cutover

[Bead Pages](../README.md) / [bob-cli-nb](README.md) / bob-cli-nb.5

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1e2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1e2.md) · **Assignee:** `bob-cli-nb.5` · **Size:** small
**Created:** 2026-11-18 13:06:51 EST
**Plan:** [202611/bob\_tick.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bob_tick.md)

## Description

mac_cutover: once the Mac's bob has the gates build (wait with a monitor if not), replace the four Mac cron jobs with one */5 bob-tick job, delete the Highlights shell wrapper and its test, update the Mac-schedule doc sections, converge with cronctl, verify, and remove the stale bob_sync wrappers.

## Dependencies

- **Depends on:** [bob-cli-nb.2](bob-cli-nb.2.md) ◐ · ⧖ 2026-11-18
- **Depends on:** [bob-cli-nb.3](bob-cli-nb.3.md) ✓ · ⧖ 2026-11-18
- **Depends on:** [bob-cli-nb.4](bob-cli-nb.4.md) ◐ · ⧖ 2026-11-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-nb.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-nb.5/README.md) | [bob-cli-nb.5](bob-cli-nb.5.md) | 0 |
