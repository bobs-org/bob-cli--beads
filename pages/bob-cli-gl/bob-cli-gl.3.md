# Bead: bob-cli-gl.3 — Move engine slots, eligibility API, batch move helper, and parent-last writes

[Bead Pages](../README.md) / [bob-cli-gl](README.md) / bob-cli-gl.3

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.35.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.35.linker.w0.md) · **Assignee:** `bob-cli-gl.3` · **Size:** medium
**Created:** 2026-11-03 13:39:31 EST
**Plan:** [202611/capture\_move\_bullets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_move_bullets.md)

## Description

cli-engine: Extend the task-move engine with capture-only slot placement and a refuse-on-ID-collision mode. Add the shared movable-root eligibility API. Extract a `capture::batch_move` helper from inbox routing (snapshot, plan, staged postimages, `stamp_fresh` roots), and make the capture batch replace every move destination before its source. Inbox routing keeps identical behavior.

## Dependencies

- **Depends on:** [bob-cli-gl.1](bob-cli-gl.1.md) ✓ · ⧖ 2026-11-03
- **Blocks:** [bob-cli-gl.4](bob-cli-gl.4.md) ◐ · ⧖ 2026-11-03
- **Blocks:** [bob-cli-gl.5](bob-cli-gl.5.md) ◐ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-gl.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-gl.3/README.md) | [bob-cli-gl.3](bob-cli-gl.3.md) | 0 |
