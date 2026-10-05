# Bead: bob-cli-4i.3 — Serve the \`task\_complete\` picker from capture-complete

[Bead Pages](../README.md) / [bob-cli-4i](README.md) / bob-cli-4i.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.5a](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.5a.md) · **Assignee:** `bob-cli-4i.3` · **Size:** medium
**Created:** 2026-10-05 15:13:24 EDT · **Closed:** 2026-10-05 16:04:44 EDT
**Plan:** [202610/bang\_task\_complete.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bang_task_complete.md)

## Description

picker_contract: in bob-cli, add the vault-wide completable-task catalog with today's Task Link annotations (running/worked/queued/noted), the today-first ordering and ranking, the `task_complete` capture-complete context with `picker` descriptor and continuation keys, `already_selected` and recurring guards, `complete_replacement` on capture-task-id, shell completion for `!`, tests, and docs.

## Notes

[2026-10-05T20:04:26Z · bob-cli-4i.3] PROPOSED FOLLOW-UP: just test failure native::completion::kinds::tests::every_value_arg_has_a_decision (highlights create:audio kinds decision) — fails identically with this phase tree, file untouched; already tracked on bob-cli-4i.2 note #1

[2026-10-05T20:04:31Z · bob-cli-4i.3] PROPOSED FOLLOW-UP: just lint deny clippy::overly_complex_bool_expr at tests/cli/capture/pomodoro_name.rs:808 — file untouched by picker_contract; already tracked on bob-cli-4i.2 note #2

[2026-10-05T20:04:44Z · bob-cli-4i.3] picker_contract done: vault-wide completable catalog with today roles/order/ranking, task_complete capture-complete context with vault picker descriptor and !/[ continuation keys on bare !, already_selected+recurring guards, complete_replacement on capture-task-id, shell completion via !prefix. Verified: 10 new catalog unit tests + 7 new CLI tests green, full cli suite 978 green, just fmt clean; just test/lint fail only on the two pre-existing base failures recorded as PROPOSED FOLLOW-UP (4i.2 notes #1 #2). No epic-symbols.

## Dependencies

- **Depends on:** [bob-cli-4i.2](bob-cli-4i.2.md) ✓ · ⧖ 2026-10-05
- **Blocks:** [bob-cli-4i.6](bob-cli-4i.6.md) ◐ · ⧖ 2026-10-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-4i.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-4i.3/README.md) | [bob-cli-4i.3](bob-cli-4i.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`40e561f`](https://github.com/bobs-org/bob-cli/commit/40e561f850e17eb431570dff23b79b8015183f8b) | feat(capture): serve the task\_complete picker from capture-complete | [bob-cli-4i.3](bob-cli-4i.3.md) | 2026-10-05 16:06:03 EDT |
