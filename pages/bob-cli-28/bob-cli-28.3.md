# Bead: bob-cli-28.3 — Parse, completion, rewrite, help, and docs for the new forms

[Bead Pages](../README.md) / [bob-cli-28](README.md) / bob-cli-28.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0t3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0t3.md) · **Assignee:** `bob-cli-28.3` · **Size:** medium
**Created:** 2026-09-27 10:38:09 EDT · **Closed:** 2026-09-27 12:18:00 EDT
**Plan:** [202609/active\_task\_link.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/active_task_link.md)

## Description

editor-contract: expose the `pomodoro_link` mode, `^` spans, needs and diagnostics in capture-parse, the `active_task` full-completion context in capture-complete, a rewrite guard, help text, and docs.

## Notes

[2026-09-27T16:18:00Z · bob-cli-28.3] Editor contract wired: capture-parse reports pomodoro_link for solo @/^ items (active_task_route/block_id spans, active_task/pomodoro_name needs, invalid_pomodoro_link diagnostics), capture-complete offers active_task candidates backed by discovery with suffix-preserving ranges, rewrite returns the pomodoro-link non-absorbable notice, help and docs/README updated. Verified: cargo fmt clean, clippy no new warnings, full cargo test green (921 lib + 485 cli), no epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-28.2](bob-cli-28.2.md) ✓ · ⧖ 2026-09-27
- **Blocks:** [bob-cli-28.4](bob-cli-28.4.md) ◐ · ⧖ 2026-09-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-28.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-28.3/README.md) | [bob-cli-28.3](bob-cli-28.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a819093`](https://github.com/bobs-org/bob-cli/commit/a81909326b42061370d27c1ec9ded5221866f93c) | feat(capture): solo pomodoro links for existing tasks | [bob-cli-28.3](bob-cli-28.3.md) | 2026-09-27 12:20:55 EDT |
