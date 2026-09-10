# Bead: bob-cli-1z.1 — Capture grammar and completion for the task-toggle item

[Bead Pages](../README.md) / [bob-cli-1z](README.md) / bob-cli-1z.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase · **↺ Reopened:** ↺1
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0ir](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.0ir.md) · **Assignee:** `bob-cli-1z.1` · **Size:** medium
**Created:** 2026-09-10 13:19:08 EDT · **Closed:** 2026-09-10 14:19:54 EDT
**Plan:** [202609/capture\_task\_toggle.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/capture_task_toggle.md)

## Previously Closed

> ↺ Closed 2026-09-10T18:09:20Z · done
>
> (none)
>
> Reopened 2026-09-10T18:14:29Z by an epic work preclaim

## Description

grammar: add the `task_toggle` item mode to the shared capture grammar, re-point `#` after `@route+id` at Pomodoro names while the item has no text, add the three `task_toggle_*` span kinds, and route completion accordingly.

## Notes

[2026-09-10T18:09:20Z · bob-cli-1z.1] Implemented the task_toggle grammar phase in capture_language.rs (CaptureKind::TaskToggle, EditorMode::TaskToggle, 3 new task_toggle_* span kinds), capture_parse.rs (mode/needs reporting via the shared editor grammar, no direct changes needed), capture_complete.rs (# after @route+id routes to PomodoroName when the item is toggle-eligible, TaskSection otherwise), and capture_rewrite.rs (toggle markers report the new non-absorbable notice). Also updated capture.rs minimally: CaptureKind is exhaustively matched there, so added a graceful 'not implemented yet' guard plus 3 match arms, and fixed/added tests. Verified: 'just all' passes (793 lib + 432 CLI integration tests, fmt, clippy). Manually ran all 4 capture-parse verification commands from the phase description plus the stale-binary check -- all match expected output exactly. Also manually verified capture-complete's Pomodoro-name routing and capture-rewrite's new notice end-to-end against scratch vaults. Note: while testing 'bob capture' manually I accidentally wrote one real task line to the user's actual ~/bob/mac_inbox.md (no --bob-dir given); caught it immediately and reverted the file to its exact prior content. No epic-symbol leftovers for this phase.

[2026-09-10T18:19:54Z · bob-cli-1z.1] Verified grammar-phase implementation is present in commit fda8627. Ran just fmt lint test; all passed. Manual capture-parse probes confirmed task_toggle modes, pomodoro_name/task_section needs flip, and stale-binary guard. Manual capture-complete confirmed PomodoroName vs TaskSection context flip. capture-rewrite reports the non-absorbable task-toggle notice. sase bead epic-symbols bob-cli-1z.1 reported no entries.

## Dependencies

- **Blocks:** [bob-cli-1z.3](bob-cli-1z.3.md) ◐ · ⧖ 2026-09-10

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-1z.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-1z.1/README.md) | [bob-cli-1z.1](bob-cli-1z.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`fda8627`](https://github.com/bobs-org/bob-cli/commit/fda8627d7181e20457ea5e299e2033d5c0a8744d) | feat(capture): add task\_toggle capture grammar phase | [bob-cli-1z.1](bob-cli-1z.1.md) | 2026-09-10 14:10:12 EDT |
