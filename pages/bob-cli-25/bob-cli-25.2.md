# Bead: bob-cli-25.2 — Project-note content renderer

[Bead Pages](../README.md) / [bob-cli-25](README.md) / bob-cli-25.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.1a](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.apollo.1a.md) · **Assignee:** `bob-cli-25.2` · **Size:** medium
**Created:** 2026-09-20 18:07:12 EDT · **Closed:** 2026-09-20 18:25:56 EDT
**Plan:** [202609/capture\_project\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/capture_project_notes.md)

## Description

render: add a pure module that derives the project-note basename and renders its frontmatter, `^prj` task, `## Tasks` entries, and ALL-CAPS section headers from a parsed capture item.

## Notes

[2026-09-20T22:25:56Z · bob-cli-25.2] Added src/native/capture_project_note.rs (pure renderer: basename, frontmatter, prj line, Tasks, ALL-CAPS sections, placeholder) with 15 unit tests; full cargo test green (894 lib + 457 cli + parity suites), rustfmt clean on new file, one-line mod registration in src/native.rs

## Dependencies

- **Blocks:** [bob-cli-25.3](bob-cli-25.3.md) ✓ · ⧖ 2026-09-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-25.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-25.2/README.md) | [bob-cli-25.2](bob-cli-25.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`2393e8a`](https://github.com/bobs-org/bob-cli/commit/2393e8a65317167fd539e92bf1a3235654bac191) | feat(capture): add project-note content renderer | [bob-cli-25.2](bob-cli-25.2.md) | 2026-09-20 18:26:50 EDT |
