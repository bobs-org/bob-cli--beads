# Bead: bob-cli-gl.3 — Move engine slots, eligibility API, batch move helper, and parent-last writes

[Bead Pages](../README.md) / [bob-cli-gl](README.md) / bob-cli-gl.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.35.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.35.linker.w0.md) · **Assignee:** `bob-cli-gl.3` · **Size:** medium
**Created:** 2026-11-03 13:39:31 EST · **Closed:** 2026-11-03 14:27:08 EST
**Plan:** [202611/capture\_move\_bullets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_move_bullets.md)

## Description

cli-engine: Extend the task-move engine with capture-only slot placement and a refuse-on-ID-collision mode. Add the shared movable-root eligibility API. Extract a `capture::batch_move` helper from inbox routing (snapshot, plan, staged postimages, `stamp_fresh` roots), and make the capture batch replace every move destination before its source. Inbox routing keeps identical behavior.

## Notes

[2026-11-03T19:27:08Z · bob-cli-gl.3] Implemented capture task-move slots, refuse-on-ID-collision mode, shared movable-root eligibility, and capture batch_move staging with destinations replaced before sources. Verified cargo check --lib, 1185 passed/1 ignored in the capture_-filtered library suite, all 43 task_move tests, all 5 inbox_route tests, and the batch replacement-order test. epic-symbols reported no leftovers.

## Dependencies

- **Depends on:** [bob-cli-gl.1](bob-cli-gl.1.md) ✓ · ⧖ 2026-11-03
- **Blocks:** [bob-cli-gl.4](bob-cli-gl.4.md) ◐ · ⧖ 2026-11-03
- **Blocks:** [bob-cli-gl.5](bob-cli-gl.5.md) ◐ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-gl.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-gl.3/README.md) | [bob-cli-gl.3](bob-cli-gl.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`cf1e464`](https://github.com/bobs-org/bob-cli/commit/cf1e46442bf7dca5bedfeeba9571ca3b5b3bbc37) | feat(capture): add ordered batch task moves | [bob-cli-gl.3](bob-cli-gl.3.md) | 2026-11-03 14:28:20 EST |
