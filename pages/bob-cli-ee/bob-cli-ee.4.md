# Bead: bob-cli-ee.4 — Bob Mac Capture t:\<type\> painting, type menu, and preview

[Bead Pages](../README.md) / [bob-cli-ee](README.md) / bob-cli-ee.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.b6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.b6.md) · **Assignee:** `bob-cli-ee.4` · **Size:** large
**Created:** 2026-10-30 04:22:33 EDT · **Closed:** 2026-10-30 13:05:58 EDT
**Plan:** [202610/capture\_type\_marker.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_type_marker.md)

## Description

mac: decode the new contract, paint `t:` markers as type pills, open a compact task-type menu with a consequence footer and Ctrl+D hide, render the type row and ledger relocation in previews, and document and test it all.

## Notes

[2026-10-30T15:42:12Z · bob-cli-ee.4] PROPOSED FOLLOW-UP: Skipped task-type marker decision memory — epic memory_record=no forbids adding decisions:type-marker-is-orthogonal; land agent may triage the orthogonality, named-Pomodoro agreement, and no-prefix-resolution record after implementation.

[2026-10-30T17:05:58Z · bob-cli-ee.4] Mac thin-client t:<type> painting, compact task-type menu, Type/ledger preview rows, notifications, docs, and 33 Bob-generated fixtures landed.

Verified: athena just portable-check 1800 tests 0 failures (CaptureTaskTypeTests 19/19); Mac scratch just typecheck-tests PASS; just docs-test OK; just docs-check OK against cached bob-cli master.

PROPOSED FOLLOW-UP: bob-cli debug_assert panics in src/native/capture/pomodoro_blocks.rs:662 on running-entry type relocation outcomes rename_entry, append_component, and rename_placeholder, and line 809 on create_below. Only move_to succeeds under debug assertions. Task-type relocation fixtures were generated with CARGO_PROFILE_DEV_DEBUG_ASSERTIONS=false.

## Dependencies

- **Depends on:** [bob-cli-ee.1](bob-cli-ee.1.md) ✓ · ⧖ 2026-10-30
- **Depends on:** [bob-cli-ee.2](bob-cli-ee.2.md) ✓ · ⧖ 2026-10-30
- **Depends on:** [bob-cli-ee.3](bob-cli-ee.3.md) ✓ · ⧖ 2026-10-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ee.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ee.4.md) | [bob-cli-ee.4](bob-cli-ee.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@68aa63a`](https://github.com/bobs-org/bob-mac-capture/commit/68aa63a1536b677f4ed57d8492864665a3bb73f8) | feat(capture): present t:\<type\> menu, pills, and relocation preview | [bob-cli-ee.4](bob-cli-ee.4.md) | 2026-10-30 13:23:23 EDT |
