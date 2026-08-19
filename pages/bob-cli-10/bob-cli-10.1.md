# Bead: bob-cli-10.1 — Shared task-section scanner in bob-cli

[Bead Pages](../README.md) / [bob-cli-10](README.md) / bob-cli-10.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.085](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.085.md) · **Assignee:** `bob-cli-10.1` · **Size:** small
**Created:** 2026-08-19 16:04:39 EDT · **Closed:** 2026-08-19 16:24:02 EDT
**Plan:** [202608/capture\_task\_sections.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/capture_task_sections.md)

## Description

sections_core: add one authoritative bob-cli module that enumerates a task's ALL-CAPS child section bullets using the same title whitelist the bob-navigation-hotkeys Ctrl+Shift+Alt+N conversion uses, plus a canonical whitespace-free slug, selector matching, and insertion geometry, covered by unit tests and used by no CLI surface yet.

## Notes

[2026-08-19T20:24:02Z · bob-cli-10.1] Added src/native/capture_task_sections.rs as the sole owner of the task-section title predicate (plugin PROJECT_SECTION_TITLE_RE plus at-least-one-letter, checkbox strip, no nested-child lookahead), slug, direct-child enumeration via nearest_shallower_list_item_parent, whole-slug-then-prefix selector matching, and section insertion geometry reusing capture.rs helpers. Registered the module after capture_task_id with no CLI surface. Unit tests cover whitelist edges, checkboxes, grandchildren, empty sections, ordered/*/+ markers, tab/2-space/4-space/mixed indent, every managed-log spelling plus plain SCHEDULE/WORK LOG, slug-prefix vs exact, duplicate slugs, middle/last/blank/managed-log insertion offsets, and CRLF. just fmt, just lint, just test, and git diff --check passed.

[2026-08-19T20:25:11Z · bob-cli-10.1] Added src/native/capture_task_sections.rs as the sole owner of the task-section title predicate (plugin PROJECT_SECTION_TITLE_RE plus at-least-one-letter, checkbox strip, no nested-child lookahead), slug, direct-child enumeration via nearest_shallower_list_item_parent, whole-slug-then-prefix selector matching, and section insertion geometry reusing capture.rs helpers. Registered the module after capture_task_id with no CLI surface. Unit tests cover whitelist edges, checkboxes, grandchildren, empty sections, ordered/*/+ markers, tab/2-space/4-space/mixed indent, every managed-log spelling plus plain SCHEDULE/WORK LOG, slug-prefix vs exact, duplicate slugs, middle/last/blank/managed-log insertion offsets, and CRLF. just fmt, just lint, just test, and git diff --check passed. No leftover --epic-symbol entries.

## Dependencies

- **Blocks:** [bob-cli-10.2](bob-cli-10.2.md) ✓ · ⧖ 2026-08-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-10.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-10.1/README.md) | [bob-cli-10.1](bob-cli-10.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d138e5a`](https://github.com/bobs-org/bob-cli/commit/d138e5a83965a3a676b5ee392a1162bcfae3a775) | feat(capture): add shared task-section scanner module | [bob-cli-10.1](bob-cli-10.1.md) | 2026-08-19 16:25:37 EDT |
