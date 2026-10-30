# Bead: bob-cli-e8.2 — Rust mention scanner, reserved label, and writer guards

[Bead Pages](../README.md) / [bob-cli-e8](README.md) / bob-cli-e8.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2v.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2v.linker.w0.md) · **Assignee:** `bob-cli-e8.2` · **Size:** medium
**Created:** 2026-10-29 17:20:21 EDT · **Closed:** 2026-10-29 20:02:17 EDT
**Plan:** [202610/inline\_task\_mentions.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/inline_task_mentions.md)

## Description

cli-core: add task_relations/mentions.rs driven by the shared vectors, reserve 💬 labels in every parser and authored writer, and stop relations reverse from dropping mention entries.

## Notes

[2026-10-29T23:49:41Z · bob-cli-e8.2--5] PROPOSED FOLLOW-UP: Clean base commit 53bf3dfa reproduces the same 12 unrelated cargo test --test cli failures seen in just check: capture plan-budget (3), pomodoro close selection, task-complete human output, task-theme writes (4), catalog protocol 1, plan human budget, and ref-library today. Keep this phase scoped to mention work; repair those baseline failures separately.

[2026-10-30T00:02:17Z · bob-cli-e8.2--7] Rust mention scanner, typed parser, reserved-label guards, and reverse-writer preservation completed. Task-relations and relation-label suites passed; isolated shell-completion test passed. The 12 CLI failures reproduce on clean base 53bf3dfa and remain in the proposed follow-up; the additional shell-completion failure passed in isolation and is intermittent/unrelated. Epic symbols clear.

## Dependencies

- **Depends on:** [bob-cli-e8.1](bob-cli-e8.1.md) ✓ · ⧖ 2026-10-29
- **Blocks:** [bob-cli-e8.3](bob-cli-e8.3.md) ◐ · ⧖ 2026-10-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-e8.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-e8.2.md) | [bob-cli-e8.2](bob-cli-e8.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`41338bc`](https://github.com/bobs-org/bob-cli/commit/41338bcfdf28959528b3f94471e2f16928ae53b6) | feat(task-relations): parse and preserve text mentions | [bob-cli-e8.2](bob-cli-e8.2.md) | 2026-10-29 20:03:12 EDT |
