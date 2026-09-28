# Bead: bob-cli-2a.2 — Expose and document the session-operator contract

[Bead Pages](../README.md) / [bob-cli-2a](README.md) / bob-cli-2a.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.2k](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.2k.md) · **Assignee:** `bob-cli-2a.2` · **Size:** medium
**Created:** 2026-09-28 10:35:57 EDT · **Closed:** 2026-09-28 11:16:49 EDT
**Plan:** [202609/pomodoro\_shift\_operators.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/pomodoro_shift_operators.md)

## Description

editor_contract: surface `pomodoro_shift` mode, span, spec, and diagnostics in capture-parse, make bare `+`/`-`/`++`/`--` complete editor states, keep completion/rewrite/`@@` away from operator items, and update every help text, docs/capture.md, and README with protocol tests.

## Notes

[2026-09-28T15:16:31Z · bob-cli-2a.2] PROPOSED FOLLOW-UP: just lint fails identically on the clean base tree (clippy overly_complex_bool_expr deny at tests/cli.rs:31812, `|| true` in an unrelated assertion); tracked under clippy-cleanup bead bob-cli-v

[2026-09-28T15:16:49Z · bob-cli-2a.2] Editor contract done: capture-parse reports pomodoro_shift mode/span/spec (additive, schema v1) plus invalid_pomodoro_shift diagnostics, human shift line with singular/plural units (also fixed adjust singular); capture/capture-complete help teach +[N]/-[N]/++[N]/--[N] with --1 CLI note; parity inputs extended; docs/capture.md gains shift section/rows/parse contract and README matches. Verified: just fmt clean, just test green (967 lib + 506 cli incl. 3 new shift protocol tests), epic-symbols empty; just lint deny is pre-existing on clean tree (noted, bob-cli-v).

## Dependencies

- **Depends on:** [bob-cli-2a.1](bob-cli-2a.1.md) ✓ · ⧖ 2026-09-28
- **Blocks:** [bob-cli-2a.3](bob-cli-2a.3.md) ✓ · ⧖ 2026-09-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2a.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2a.2/README.md) | [bob-cli-2a.2](bob-cli-2a.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0dfbc55`](https://github.com/bobs-org/bob-cli/commit/0dfbc55dad5a21faeb988e6d180fa007d312ddea) | feat(capture): expose and document the Pomodoro shift editor contract | [bob-cli-2a.2](bob-cli-2a.2.md) | 2026-09-28 11:19:35 EDT |
