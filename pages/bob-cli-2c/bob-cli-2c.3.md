# Bead: bob-cli-2c.3 — Expose and document the Pomodoro start editor contract

[Bead Pages](../README.md) / [bob-cli-2c](README.md) / bob-cli-2c.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.2s](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.2s.md) · **Assignee:** `bob-cli-2c.3` · **Size:** medium
**Created:** 2026-09-28 12:19:13 EDT · **Closed:** 2026-09-28 13:13:02 EDT
**Plan:** [202609/pomodoro\_start\_next\_operator.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/pomodoro_start_next_operator.md)

## Description

editor_contract: teach capture-parse, completion, and rewrite the whole-item start (mode, span, spec, diagnostics, @@ skip), update help, docs/capture.md, and README with the lifecycle table and zsh quoting, and add protocol tests.

## Notes

[2026-09-28T17:12:45Z · bob-cli-2c.3] PROPOSED FOLLOW-UP: cargo clippy --all-targets fails on base tree at tests/cli.rs:31812 overly_complex_bool_expr (|| true); pre-existing, unrelated to editor_contract

[2026-09-28T17:13:02Z · bob-cli-2c.3] Editor contract done: =-family parser reports pomodoro_start specs/spans/diagnostics, @@ skip, no completion/rewrite, lifecycle help with zsh note, docs/capture.md Starting section, README grammar; verified cargo fmt --check, 1036 lib + 515 cli tests pass including 3 new start protocol tests

## Dependencies

- **Depends on:** [bob-cli-2c.2](bob-cli-2c.2.md) ✓ · ⧖ 2026-09-28
- **Blocks:** [bob-cli-2c.4](bob-cli-2c.4.md) ◐ · ⧖ 2026-09-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2c.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2c.3/README.md) | [bob-cli-2c.3](bob-cli-2c.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d223926`](https://github.com/bobs-org/bob-cli/commit/d22392671b5e92dadbafd2585cb797bbd017f459) | feat(capture): expose and document the Pomodoro start editor contract | [bob-cli-2c.3](bob-cli-2c.3.md) | 2026-09-28 13:14:29 EDT |
