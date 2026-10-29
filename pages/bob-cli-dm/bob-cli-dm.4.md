# Bead: bob-cli-dm.4 — Capture remembers deliberate \`#NAME\` choices

[Bead Pages](../README.md) / [bob-cli-dm](README.md) / bob-cli-dm.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2s.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2s.linker.w0.md) · **Assignee:** `bob-cli-dm.4` · **Size:** large
**Created:** 2026-10-28 08:45:53 EDT · **Closed:** 2026-10-28 19:44:08 EDT
**Plan:** [202610/task\_theme\_suggestions.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_theme_suggestions.md)

## Description

capture-write: apply the write rule when a capture names a Pomodoro for a new or existing task (`#NAME` and the `=name` shorthand), staged in the same all-or-nothing batch, reported as `task_theme` in JSON, human, and dry-run output.

## Notes

[2026-10-28T23:44:08Z · bob-cli-dm.4--1] Implemented deliberate capture task-theme writes for explicit #NAME and =name, staged theme-ledger changes with capture writes, and documented behavior. Verified cargo test --test cli capture::task_theme_writes (7 passed), just all (passed), just docs-check (passed), and git diff --check.

## Dependencies

- **Depends on:** [bob-cli-dm.2](bob-cli-dm.2.md) ✓ · ⧖ 2026-10-28
- **Depends on:** [bob-cli-dm.3](bob-cli-dm.3.md) ✓ · ⧖ 2026-10-28
- **Blocks:** [bob-cli-dm.8](bob-cli-dm.8.md) ✓ · ⧖ 2026-10-28
- **Blocks:** [bob-cli-dm.9](bob-cli-dm.9.md) ◐ · ⧖ 2026-10-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-dm.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-dm.4.md) | [bob-cli-dm.4](bob-cli-dm.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`41cc4ac`](https://github.com/bobs-org/bob-cli/commit/41cc4accb121dbed65747c020f573292d2b50634) | feat(capture): add task-theme capture writes | [bob-cli-dm.4](bob-cli-dm.4.md) | 2026-10-28 19:45:54 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-dm.4--1][1] | Need the approved capture task-theme plan and completion criteria | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-dm.4.md

<!-- sase:referenced-by:end -->
