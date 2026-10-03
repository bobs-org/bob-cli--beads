# Bead: bob-cli-41.1 — Define plus task discovery and cursor contract in bob-cli

[Bead Pages](../README.md) / [bob-cli-41](README.md) / bob-cli-41.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0vw](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0vw.md) · **Assignee:** `bob-cli-41.1` · **Size:** medium
**Created:** 2026-10-03 16:24:17 EDT · **Closed:** 2026-10-03 17:08:02 EDT
**Plan:** [202610/plus\_task\_picker.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/plus_task_picker.md)

## Description

plus_completion_contract: add the shared selector classifier, additive completion metadata, vault-wide discovery adapter, backend-authored ID assignment replacement, and Rust contract/regression tests.

## Notes

[2026-10-03T21:07:49Z · bob-cli-41.1] PROPOSED FOLLOW-UP: Investigate completion::zsh_adapter::default_styles_use_green_headers — full cargo test fails identically on the clean base because zstyle -L omits the expected %B%F{green} header; no existing task bead tracks this test.

[2026-10-03T21:08:02Z · bob-cli-41.1] Implemented bare-plus parent-task discovery and completion metadata, ID assignment replacements, parser safeguards, docs, and regression coverage. Verified cargo fmt --check; cargo clippy --all-targets --all-features; 8 Pomodoro shift, 8 parent/selector unit, and 15 parent-related CLI tests. Full cargo test comparison against clean base: both passed all 1,620 unit tests and failed only completion::zsh_adapter::default_styles_use_green_headers among 925 CLI tests; proposed follow-up recorded. epic-symbols had no entries.

## Dependencies

- **Blocks:** [bob-cli-41.2](bob-cli-41.2.md) ✓ · ⧖ 2026-10-03
- **Blocks:** [bob-cli-41.3](bob-cli-41.3.md) ✓ · ⧖ 2026-10-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-41.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-41.1/README.md) | [bob-cli-41.1](bob-cli-41.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0aa9b8a`](https://github.com/bobs-org/bob-cli/commit/0aa9b8a72163187de0c1c6c4796049ccd1ea9281) | feat(capture): add parent task picker | [bob-cli-41.1](bob-cli-41.1.md) | 2026-10-03 17:08:56 EDT |
