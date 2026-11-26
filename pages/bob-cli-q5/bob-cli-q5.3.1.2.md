# Bead: bob-cli-q5.3.1.2 — Apply capture snooze operations atomically

[Bead Pages](../README.md) / [bob-cli-q5.3.1](bob-cli-q5.3.1.md) / bob-cli-q5.3.1.2

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.3.md) · **Assignee:** `bob-cli-q5.3.1.2` · **Size:** medium
**Created:** 2026-11-25 19:34:28 EST
**Plan:** [202611/capture\_snooze\_token.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_snooze_token.md)

## Description

mutation: connect snooze add/drop to capture snapshots for existing and new tasks, preserve row notes when linking now, implement retime and drop, and verify refusals and whole-batch atomicity.

## Notes

[2026-11-26T08:45:04Z · bob-cli-q5.3.1.2] PROPOSED FOLLOW-UP: Numeric-route snooze-drop preview disagrees with execution — capture-parse -f json -- "@20261125:here!" returns mode=task and body="@20261125:here" while capture correctly drops the active row by basename; the editor masks the bang then falls through the existing alphabetic-route candidate guard. Existing parser code is unchanged by this mutation phase.

[2026-11-26T08:47:56Z · bob-cli-q5.3.1.2] PROPOSED FOLLOW-UP: Clarify or fix relative snooze rounding — the shared core parser rounds the duration, not the resulting wall clock: at 12:03, +45m resolves to 12:48 and +1h to 13:03. docs/snooze.md says relative targets round upward to a five-minute boundary. Capture intentionally reuses the unchanged core parser; the mutation regression pins its actual result rather than adding divergent capture-only rounding.

## Dependencies

- **Depends on:** [bob-cli-q5.3.1.1](bob-cli-q5.3.1.1.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q5.3.1.3](bob-cli-q5.3.1.3.md) ◐ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.3.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.3.1.2/README.md) | [bob-cli-q5.3.1.2](bob-cli-q5.3.1.2.md) | 0 |
