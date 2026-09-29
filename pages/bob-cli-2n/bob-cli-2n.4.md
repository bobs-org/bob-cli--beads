# Bead: bob-cli-2n.4 — Block-ID completion for project task IDs

[Bead Pages](../README.md) / [bob-cli-2n](README.md) / bob-cli-2n.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.35](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.35.md) · **Assignee:** `bob-cli-2n.4` · **Size:** small
**Created:** 2026-09-29 15:35:25 EDT · **Closed:** 2026-09-29 17:15:01 EDT
**Plan:** [202609/project\_task\_links.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/project_task_links.md)

## Description

task-id-completion: add the `project_task_block_id` capture-complete context with a `block_id` object (new intent, sibling and `prj` used IDs, body-derived suggestions) so editors can offer a New ID picker after ` :` or ` ^`.

## Notes

[2026-09-29T21:14:46Z · bob-cli-2n.4] PROPOSED FOLLOW-UP: clippy deny clippy::overly_complex_bool_expr on tests/cli/capture/pomodoro_name.rs:808 (`|| true`); reproduces identically on the clean base tree, unrelated to this phase

[2026-09-29T21:15:01Z · bob-cli-2n.4] Implemented project_task_block_id capture-complete context (new CompletionContext variant, child-line detection reusing project_tasks lexer, block_id builder with intent new / stem route / sigil range / checkbox-stripped body / prj+sibling used / suggest_ids suggestions, help text). Verified: 5 new completion unit tests + new CLI JSON test pass; full cargo test green (1187 lib + 540 cli, 0 failures); cargo fmt clean; clippy clean for touched files (one pre-existing deny in untouched pomodoro_name.rs:808 recorded as follow-up, reproduces on clean base); epic-symbols empty.

## Dependencies

- **Depends on:** [bob-cli-2n.2](bob-cli-2n.2.md) ✓ · ⧖ 2026-09-29
- **Blocks:** [bob-cli-2n.5](bob-cli-2n.5.md) ✓ · ⧖ 2026-09-29
- **Blocks:** [bob-cli-2n.6](bob-cli-2n.6.md) ✓ · ⧖ 2026-09-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2n.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2n.4/README.md) | [bob-cli-2n.4](bob-cli-2n.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`301e809`](https://github.com/bobs-org/bob-cli/commit/301e809053278768e46263d03f127b930acc4e41) | feat(capture): add project\_task\_block\_id capture-complete context | [bob-cli-2n.4](bob-cli-2n.4.md) | 2026-09-29 17:16:19 EDT |
