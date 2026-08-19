# Bead: bob-cli-10.4 — \`bob capture-task-sections\` and \`task\_section\` completion

[Bead Pages](../README.md) / [bob-cli-10](README.md) / bob-cli-10.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.085](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.085.md) · **Assignee:** `bob-cli-10.4` · **Size:** medium
**Created:** 2026-08-19 16:04:39 EDT · **Closed:** 2026-08-19 17:33:37 EDT
**Plan:** [202608/capture\_task\_sections.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/capture_task_sections.md)

## Description

discovery: add the read-only `bob capture-task-sections` subcommand and the `task_section` context in `bob capture-complete`, both backed by the shared scanner, with slug replacements, deterministic ranking, bounded warnings for an unresolvable parent task, registration in the command table and install smoke test, documentation, and integration tests.

## Notes

[2026-08-19T21:33:37Z · bob-cli-10.4] Added read-only bob capture-task-sections (exactly one of -i/--block-id or -t/--task-ref; parent lookup/errors match bob capture; JSON schema_version 1 with title/slug/line/child_count/depth=1; empty list for a task with no sections) and capture-complete task_section candidates (slug replacement, prefix-then-substring ranking, empty success for @route+#, one bounded warning for an unresolvable parent). Registered in native.rs, runner.rs, justfile install-smoke, README, and help tables. Verified with just fmt, just lint, just test, just install-smoke, and git diff --check.

[2026-08-19T21:37:08Z · bob-cli-10.4] Added read-only bob capture-task-sections (exactly one of -i/--block-id or -t/--task-ref; parent lookup/errors match bob capture; JSON schema_version 1 with title/slug/line/child_count/depth=1; empty list for a task with no sections) and capture-complete task_section candidates (slug replacement, prefix-then-substring ranking, empty success for @route+#, one bounded warning for an unresolvable parent). Registered in native.rs, runner.rs, justfile install-smoke, README, and help tables. Verified with just fmt, just lint, just test, just install-smoke, and git diff --check.

## Dependencies

- **Depends on:** [bob-cli-10.2](bob-cli-10.2.md) ✓ · ⧖ 2026-08-19
- **Blocks:** [bob-cli-10.5](bob-cli-10.5.md) ✓ · ⧖ 2026-08-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-10.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-10.4/README.md) | [bob-cli-10.4](bob-cli-10.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`54e4d21`](https://github.com/bobs-org/bob-cli/commit/54e4d213bb27882239e9e61669c81c08dca00d33) | feat(capture): add capture-task-sections and task\_section completion | [bob-cli-10.4](bob-cli-10.4.md) | 2026-08-19 17:37:41 EDT |
