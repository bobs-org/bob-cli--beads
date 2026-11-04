# Bead: bob-cli-h0.5 — Mint, splice at the slot, offer exclusion, and output

[Bead Pages](../README.md) / [bob-cli-h0](README.md) / bob-cli-h0.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.37.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.37.linker.w0.md) · **Assignee:** `bob-cli-h0.5` · **Size:** medium
**Created:** 2026-11-04 08:50:24 EST · **Closed:** 2026-11-04 13:55:40 EST
**Plan:** [202611/move\_choice.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/move_choice.md)

## Description

cli-execute: mint IDs for picked ID-less rows, splice picks into the move list at the `^^` slot in parent order, keep them out of successor offers, enforce the `#name` backstop, report `via: "choice"`, and pin MQ equivalence.

## Notes

[2026-11-04T18:55:01Z · bob-cli-h0.5] PROPOSED FOLLOW-UP: Pre-existing `cargo fmt --check` drift in untouched files (draft.rs, editor_pomodoro.rs, past.rs, item.rs lines outside h0.5 edits, parse_pomodoro_past.rs) makes `just check` fmt gate red on clean tree; needs a formatting pass (no task bead cited)

[2026-11-04T18:55:12Z · bob-cli-h0.5] PROPOSED FOLLOW-UP: Pre-existing clippy deny failures (8 errors, all in untouched src/native/capture_language/editor_pomodoro.rs: needless_return, collapsible_if, question_mark) make `just check` clippy gate red on clean tree

[2026-11-04T18:55:18Z · bob-cli-h0.5] PROPOSED FOLLOW-UP: Pre-existing `just docs-check` strict Zensical build failure on untouched docs/reference/mac-capture/keyboard.md:104 anchor `#going-to-a-task-from-any-app-command--then-` does not exist; lint and generated drift pass

[2026-11-04T18:55:40Z · bob-cli-h0.5] cli-execute done: pre-pass mints ID-less picks into staged parent and splices synthetic via:Choice moves at ^^ in parent order; offers exclude Choice rows; #name backstop enforced; moved_tasks gain via choice/bullet with ^^ draft_range and added-ID detail. Verified MQ7 byte-identical dest/source, MQ8 parent-order splice, MQ9 mint and collision, MQ10 offer exclusion, MQ12 disabled, MQ16 :1 links, MQ17 predict==outcome; 5 choice + 44 project_note tests green; capture help + golden updated; interim unavailable removed. Pre-existing fmt/clippy/docs-build failures filed as follow-ups.

## Dependencies

- **Depends on:** [bob-cli-h0.4](bob-cli-h0.4.md) ✓ · ⧖ 2026-11-04
- **Blocks:** [bob-cli-h0.8](bob-cli-h0.8.md) ◐ · ⧖ 2026-11-04

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-h0.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-h0.5/README.md) | [bob-cli-h0.5](bob-cli-h0.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`458b53b`](https://github.com/bobs-org/bob-cli/commit/458b53b95188cd986513a64d46c33336f79daf35) | feat(capture): execute move\_choice picks with mint, splice, offers and via | [bob-cli-h0.5](bob-cli-h0.5.md) | 2026-11-04 13:57:24 EST |
