# Bead: bob-cli-5y.12 — Bob Mac Capture asks where a captured link belongs

[Bead Pages](../README.md) / [bob-cli-5y](README.md) / bob-cli-5y.12

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0z0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0z0.md) · **Assignee:** `bob-cli-5y.12` · **Size:** medium
**Created:** 2026-10-09 12:29:34 EDT · **Closed:** 2026-10-09 21:56:44 EDT
**Plan:** [202610/ref\_tasks\_live\_with\_parent.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_tasks_live_with_parent.md)

## Description

mac-file-under: open a File under picker for a bare URL, insert the chosen @route, preview the destination, and match project_name_aliases.

## Notes

[2026-10-10T01:34:10Z · bob-cli-5y.12] PROPOSED FOLLOW-UP: Add decisions strand ref-tasks-live-with-their-parent recording residence-is-the-parent (skipped per epic memory_ref_parent_decision=no)

[2026-10-10T01:34:14Z · bob-cli-5y.12] PROPOSED FOLLOW-UP: Update glossary strands reference-task, reference-note, area-note for the parent-residence model (skipped per epic memory_glossary_ref_terms=no)

[2026-10-10T01:56:44Z · bob-cli-5y.12--1] mac-file-under done: File-under picker opens for bare-URL ref drafts with default parent, splices @route, previews destination, matches project_name_aliases. Verified: just check exit 0 (bob-cli); swift CaptureCoreTests 903 pass incl 11 new CaptureRefFileUnderTests; real bob capture-parse output matches all 3 new fixtures (default/explicit/alias). AppKit panel tests are Xcode-only, unrunnable on Linux (environmental).

## Dependencies

- **Depends on:** [bob-cli-5y.10](bob-cli-5y.10.md) ✓ · ⧖ 2026-10-09
- **Blocks:** [bob-cli-5y.14](bob-cli-5y.14.md) ◐ · ⧖ 2026-10-09
- **Depends on:** [bob-cli-5y.8](bob-cli-5y.8.md) ✓ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-5y.12](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-5y.12.md) | [bob-cli-5y.12](bob-cli-5y.12.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@f51cdc1`](https://github.com/bobs-org/bob-mac-capture/commit/f51cdc18dc35253ced7fa0542999e4544550eb35) | feat(capture-ref): ask where a captured link belongs with File under picker | [bob-cli-5y.12](bob-cli-5y.12.md) | 2026-10-09 21:57:55 EDT |
