# Bead: bob-cli-2o.5 — bob-cli: \`~\<K\>\` drop outcome for \`=x\` closes

[Bead Pages](../README.md) / [bob-cli-2o](README.md) / bob-cli-2o.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.38](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.38.md) · **Assignee:** `bob-cli-2o.5` · **Size:** medium
**Created:** 2026-09-29 18:09:56 EDT · **Closed:** 2026-09-29 20:05:08 EDT
**Plan:** [202609/pomodoro\_plan\_budget\_now\_tag.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/pomodoro_plan_budget_now_tag.md)

## Description

close-drop: extend the close grammar to `=x[<N>][!<M>][~<K>]`, where dropped links are removed from the closed session, not carried, and not started; add editor spans, JSON (`drop`, outcome and role `dropped`, and a `now` flag on close task rows), human output, help, and docs.

## Notes

[2026-09-30T00:04:52Z · bob-cli-2o.5] PROPOSED FOLLOW-UP: clippy gate fails on clean base at tests/cli/capture/pomodoro_name.rs:808 (`|| true` logic bug) plus 18 pre-existing lib warnings; verified identical on HEAD 35b96b3 via clean worktree, close-drop adds zero new lints

[2026-09-30T00:05:08Z · bob-cli-2o.5] close-drop done: =x[<N>][!<M>][~<K>] lexes in either !/~ order with pomodoro_close_drop spans; dropped links removed via transient ~ marker (not carried, never started, no Work Log); JSON gains drop/outcome+role dropped/tasks now flag; human shows dropped rows + Dropped summary; help+docs updated. Verified: cargo test full suite green (1242 lib + 589 cli), cargo fmt clean, epic-symbols none; clippy gate failure pre-exists on base (recorded as follow-up).

## Dependencies

- **Depends on:** [bob-cli-2o.1](bob-cli-2o.1.md) ✓ · ⧖ 2026-09-29
- **Blocks:** [bob-cli-2o.12](bob-cli-2o.12.md) ✓ · ⧖ 2026-09-29
- **Depends on:** [bob-cli-2o.4](bob-cli-2o.4.md) ✓ · ⧖ 2026-09-29
- **Blocks:** [bob-cli-2o.6](bob-cli-2o.6.md) ✓ · ⧖ 2026-09-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2o.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2o.5/README.md) | [bob-cli-2o.5](bob-cli-2o.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`754d1f3`](https://github.com/bobs-org/bob-cli/commit/754d1f31fe7feffb81c85d4ed55c17888f15a65f) | feat(capture): \`~\<K\>\` drop outcome for \`=x\` closes | [bob-cli-2o.5](bob-cli-2o.5.md) | 2026-09-29 20:11:18 EDT |
