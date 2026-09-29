# Bead: bob-cli-2n.2 — Project task IDs in the capture grammar and capture-parse

[Bead Pages](../README.md) / [bob-cli-2n](README.md) / bob-cli-2n.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.35](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.35.md) · **Assignee:** `bob-cli-2n.2` · **Size:** medium
**Created:** 2026-09-29 15:35:25 EDT · **Closed:** 2026-09-29 16:57:29 EDT
**Plan:** [202609/project\_task\_links.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/project_task_links.md)

## Description

task-id-grammar: lex trailing ` :id` / ` ^id` tokens on project-note lines, enforce the placement, validity, duplicate, checkbox, and unused-`#pomodoro` rules in both the execution and editor parsers, and expose spans, needs, modes, and `sub_bullet_task_ids` through capture-parse.

## Notes

[2026-09-29T20:57:11Z · bob-cli-2n.2] PROPOSED FOLLOW-UP: default cargo clippy/test is red at HEAD on untouched tests/cli/capture/pomodoro_name.rs:808 (overly_complex_bool_expr deny: assertion ends with `|| true`), blocking `cargo test --test cli` compilation under rustc 1.95.0; this phase verified with RUSTFLAGS=--cap-lints=warn instead

[2026-09-29T20:57:29Z · bob-cli-2n.2] task-id-grammar done: shared project_tasks.rs lexer+ProjectTaskPass drives identical evaluation order in execution and editor; spans/modes/needs/sub_bullet_task_ids (top-level+per-item) live in capture-parse JSON+human+help; verified cargo fmt clean, cargo test --lib 1182 passed, cargo test --test cli 539 passed (RUSTFLAGS=--cap-lints=warn to bypass pre-existing pomodoro_name.rs:808 deny-lint, recorded as follow-up)

## Dependencies

- **Depends on:** [bob-cli-2n.1](bob-cli-2n.1.md) ✓ · ⧖ 2026-09-29
- **Blocks:** [bob-cli-2n.3](bob-cli-2n.3.md) ◐ · ⧖ 2026-09-29
- **Blocks:** [bob-cli-2n.4](bob-cli-2n.4.md) ◐ · ⧖ 2026-09-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2n.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2n.2/README.md) | [bob-cli-2n.2](bob-cli-2n.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e9c4dae`](https://github.com/bobs-org/bob-cli/commit/e9c4dae3274e09a8af0ec01762d2b35d9afd862e) | feat(capture): add project task-id grammar pass with shared lexer and editor spans | [bob-cli-2n.2](bob-cli-2n.2.md) | 2026-09-29 16:59:30 EDT |
