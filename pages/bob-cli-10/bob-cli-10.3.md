# Bead: bob-cli-10.3 — Task-section resolution and insertion in \`bob capture\`

[Bead Pages](../README.md) / [bob-cli-10](README.md) / bob-cli-10.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.085](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.085.md) · **Assignee:** `bob-cli-10.3` · **Size:** medium
**Created:** 2026-08-19 16:04:39 EDT · **Closed:** 2026-08-19 17:35:29 EDT
**Plan:** [202608/capture\_task\_sections.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/capture_task_sections.md)

## Description

execution: teach `bob capture` to resolve the selected task section and append the captured bullet inside it, add the forced `-S/--task-section TITLE` picker option, report the matched section in human and JSON output, raise actionable errors with suggestions when no section matches, and cover insertion geometry, line-ending preservation, and dry-run parity with CLI tests.

## Notes

[2026-08-19T21:35:29Z · bob-cli-10.3] Taught bob capture to insert under a resolved task section: @route+id#section uses slug/prefix matching via capture_task_sections; -S/--task-section TITLE (requires --route and --task/--task-ref, conflicts with --section) matches the whole title exactly and case-insensitively. parent_section is reported in JSON and as a cyan · TITLE suffix; omitted for plain @route+id. No-match lists titles with a close-match suggestion; no-sections has its own message; parent lookup errors still win. CLI tests cover first/middle/last, empty vs existing children, prefix vs whole-slug, multi-word, managed-log geometry, tab/two-space/four-space/CRLF, authored children, s:/p:/%/--clip, dry-run parity, forced-option errors, and failure paths leaving the note unchanged. just fmt, just lint, just test, just install-smoke, and git diff --check passed. No leftover --epic-symbol entries.

## Dependencies

- **Depends on:** [bob-cli-10.2](bob-cli-10.2.md) ✓ · ⧖ 2026-08-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-10.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-10.3/README.md) | [bob-cli-10.3](bob-cli-10.3.md) | 0 |
