# Bead: bob-cli-n5.2 — Refuse unknown short options before capture text

[Bead Pages](../README.md) / [bob-cli-n5](README.md) / bob-cli-n5.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-my.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-my.land.md) · **Assignee:** `bob-cli-n5.2` · **Size:** medium
**Created:** 2026-11-17 22:21:55 EST · **Closed:** 2026-11-18 00:02:48 EST
**Plan:** [202611/backlog\_triage\_t3.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/backlog_triage_t3.md)

## Description

short-flags: Resolve the remaining short-option half of bob-cli-8a without rejecting capture operators or literal text.

## Notes

[2026-11-18T04:15:10Z · bob-cli-n5.2] PROPOSED FOLLOW-UP: Refresh the stale docs contract registry count and README table digest — just docs-check fails in documentation unit tests: the registry has 52 entries while the test expects 51, and the README table digest differs. Reproduced identically on clean HEAD 03ab2b3d. The same c50f8895 walks-entry issue is already recorded as DISCOVERED ISSUE in bob-cli-mx note #1; closed bob-cli-hs concerns a separate schema-16 snapshot cause.

[2026-11-18T05:02:48Z · bob-cli-n5.2--2] Implemented the capture short-option guard and corrected CLI regressions that relied on undeclared option-looking tokens: capture uses -- before literal -S, and capture-parse no longer receives invalid -b. Verification passed: focused capture regressions, all 12 capture_flag_guard unit tests, just fmt, and canonical just check (exit 0).

## Dependencies

- **Depends on:** [bob-cli-n5.1](bob-cli-n5.1.md) ✓ · ⧖ 2026-11-17
- **Blocks:** [bob-cli-n5.3](bob-cli-n5.3.md) ✓ · ⧖ 2026-11-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-n5.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-n5.2.md) | [bob-cli-n5.2](bob-cli-n5.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f2a6179`](https://github.com/bobs-org/bob-cli/commit/f2a61792ad1c1cae50d9fd0cbc6ba97994c689ec) | fix(capture): guard unknown short options | [bob-cli-n5.2](bob-cli-n5.2.md) | 2026-11-18 00:03:48 EST |
