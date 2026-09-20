# Bead: bob-cli-25.1 — Project-note marker grammar

[Bead Pages](../README.md) / [bob-cli-25](README.md) / bob-cli-25.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.1a](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.apollo.1a.md) · **Assignee:** `bob-cli-25.1` · **Size:** medium
**Created:** 2026-09-20 18:07:12 EDT · **Closed:** 2026-09-20 18:43:41 EDT
**Plan:** [202609/capture\_project\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/capture_project_notes.md)

## Description

grammar: add the `+` project-note sigil to the `^` and `:` marker families in the shared capture grammar, with a new `CaptureKind`, editor modes, span kind, needs, and diagnostics.

## Notes

[2026-09-20T22:43:41Z · bob-cli-25.1] Grammar phase done: + sigil parsed into CaptureKind::ProjectNote (3 pomodoro states), project_note/pomodoro_project_note modes, project_note_marker span, invalid_project_note_marker diagnostic. Verified: full cargo test green (898 lib incl 4 new test fns + extended mode/span/diagnostic/parity tables, 458 cli incl new capture-parse JSON test), clippy clean, epic-symbols empty. capture.rs has todo! arms naming the execute phase. Note: cargo fmt --check already fails at baseline under this toolchain (import-order drift, e.g. src/lib.rs), so formatting was left as committed style with no tree-wide churn.

## Dependencies

- **Blocks:** [bob-cli-25.3](bob-cli-25.3.md) ◐ · ⧖ 2026-09-20
- **Blocks:** [bob-cli-25.5](bob-cli-25.5.md) ◐ · ⧖ 2026-09-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-25.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-25.1/README.md) | [bob-cli-25.1](bob-cli-25.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4e738fd`](https://github.com/bobs-org/bob-cli/commit/4e738fd9ab1307ad131e3395bdc911a6217138c6) | feat(capture): add project-note marker grammar | [bob-cli-25.1](bob-cli-25.1.md) | 2026-09-20 18:44:47 EDT |
