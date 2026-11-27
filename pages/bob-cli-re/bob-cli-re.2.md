# Bead: bob-cli-re.2 — Adopt fork-safe writers for the remaining executable test stubs

[Bead Pages](../README.md) / [bob-cli-re](README.md) / bob-cli-re.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-r8.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-r8.land.md) · **Assignee:** `bob-cli-re.2` · **Size:** medium
**Created:** 2026-11-27 15:31:19 EST · **Closed:** 2026-11-27 16:54:37 EST
**Plan:** [202611/task\_bead\_burndown\_3.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_bead_burndown_3.md)

## Description

executable-stubs: repair the Spotify and Gmail executable-stub races and close bob-cli-5l.

## Notes

[2026-11-27T21:34:42Z · bob-cli-re.2] PROPOSED FOLLOW-UP: lib native::config::capture type_leads tests (4) fail identically on the clean base tree; owned by active epic bob-cli-rb, not by the executable-stub race

[2026-11-27T21:44:17Z · bob-cli-re.2] PROPOSED FOLLOW-UP: cli themes type-lead tests (themes_surface_valid_type_leads, themes_rename_refusals_are_json) fail identically on the clean base tree; owned by active epic bob-cli-rb, not by the executable-stub race

[2026-11-27T21:54:37Z · bob-cli-re.2] executable-stubs phase done: ported all in-process executable-stub writers to fork-safe child-cp writers (lib via test_stub::write_executable_stub; integration via new tests/exec_stub module and tests/cli support::write_executable); closed bob-cli-5l after verification (stress test, spotify, gmail transport 5/5, all affected binaries green, full just check with zero ETXTBSY). Only failures are 6 type-lead tests failing identically on base, recorded as PROPOSED FOLLOW-UPs citing active epic bob-cli-rb. No epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-re.1](bob-cli-re.1.md) ✓ · ⧖ 2026-11-27
- **Blocks:** [bob-cli-re.3](bob-cli-re.3.md) ◐ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-re.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-re.2/README.md) | [bob-cli-re.2](bob-cli-re.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`69f8aae`](https://github.com/bobs-org/bob-cli/commit/69f8aae63cdf25cf926461f0d96a1156de1997e5) | fix(tests): eliminate ETXTBSY races via child-cp executable stubs | [bob-cli-re.2](bob-cli-re.2.md) | 2026-11-27 16:56:03 EST |
