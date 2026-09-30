# Bead: bob-cli-2v.2 — \`:\` picker-query grammar in capture, capture-parse, and completion fields

[Bead Pages](../README.md) / [bob-cli-2v](README.md) / bob-cli-2v.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.3j](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.3j.md) · **Assignee:** `bob-cli-2v.2` · **Size:** medium
**Created:** 2026-09-30 13:00:14 EDT · **Closed:** 2026-09-30 13:16:05 EDT
**Plan:** [202609/task\_link\_picker.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/task_link_picker.md)

## Description

grammar: add one claim predicate for single-token `:` items. Execution rejects them with teaching errors T1 and T2. capture-parse reports `incomplete` with `needs: ["task_link"]`. The completion field (`task_link` context) covers the sigil. Also update help text and add a claim-equivalence test.

## Notes

[2026-09-30T17:15:39Z · bob-cli-2v.2] PROPOSED FOLLOW-UP: cargo clippy --all-targets --all-features fails on clean base tree at tests/cli/capture/pomodoro_name.rs:808 (overly_complex_bool_expr deny: trailing `|| true`); tracked by bead bob-cli-v Eliminate existing bob-cli clippy warnings

[2026-09-30T17:16:05Z · bob-cli-2v.2] Grammar phase done: task_link_query_token claim shared by execution/editor/completion; T1/T2 teaching errors; editor incomplete+task_link with placeholder span; completion TaskLink context with sigil-inclusive replacement; capture-complete placeholder arm; help texts. Verified: cargo test fully green (1319 lib incl 6 new grammar/editor/completion tests, 645 cli incl 6 new task_link tests), cargo fmt clean, clippy shows only pre-existing base-tree failure (recorded as follow-up).

## Dependencies

- **Blocks:** [bob-cli-2v.4](bob-cli-2v.4.md) ◐ · ⧖ 2026-09-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2v.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2v.2/README.md) | [bob-cli-2v.2](bob-cli-2v.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`5ef8eb7`](https://github.com/bobs-org/bob-cli/commit/5ef8eb724c44a1964c2d0a0c473587bea540fe41) | feat(capture): add task-link picker query grammar for colon items | [bob-cli-2v.2](bob-cli-2v.2.md) | 2026-09-30 13:18:07 EDT |
