# Bead: bob-cli-3j.9.2 — Honest, fast bob completion lifecycle

[Bead Pages](../README.md) / [bob-cli-3j.9](bob-cli-3j.9.md) / bob-cli-3j.9.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-3j.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-3j.land.md) · **Assignee:** `bob-cli-3j.9.2` · **Size:** medium
**Created:** 2026-10-02 14:29:07 EDT · **Closed:** 2026-10-02 15:15:20 EDT
**Plan:** [202610/shell\_completion\_landing\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/shell_completion_landing_fixes.md)

## Description

lifecycle: run shell probes in their own session so they never stall under a terminal, stop status from probing or failing not-installed shells, honor $SHELL alongside owned adapters, align glyphs, exit codes, and closers with registration, keep stale compdumps visible, refuse unrecorded stamped files, and add the lifecycle tests the original plan required.

## Notes

[2026-10-02T19:15:11Z · bob-cli-3j.9.2] PROPOSED FOLLOW-UP: cargo clippy deny at tests/cli/capture/pomodoro_name.rs:808 reproduces on the clean base tree (untouched by this phase) and is owned by epic bob-cli-28 per the phase plan; completion module itself adds zero new clippy warnings

[2026-10-02T19:15:20Z · bob-cli-3j.9.2] lifecycle phase done: setsid probes with group kill and concurrent drain, stale-compdump-safe conditional compinit, no-probe not-installed status, probe-free status targets, SHELL+owned selection with -t single-shell rule, registration-honest glyphs/exit codes, truthful closers, outdated-externally-managed refusal, -t move cleanup, home-default fpath line. Verified: cargo fmt clean, full cargo test green (1522+823 incl. 94 completion tests, new zpty no-stall + 13 lifecycle tests), just install-smoke exit 0, zero new completion clippy warnings (only pre-existing bob-cli-28 deny at pomodoro_name.rs:808, noted as follow-up)

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-3j.9.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-3j.9.2/README.md) | [bob-cli-3j.9.2](bob-cli-3j.9.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8f01f33`](https://github.com/bobs-org/bob-cli/commit/8f01f331c4f81d3f2c0a1866b82f9ed161a377ef) | feat(completion): bounded probes, probe-free status, and lifecycle polish | [bob-cli-3j.9.2](bob-cli-3j.9.2.md) | 2026-10-02 15:16:32 EDT |
