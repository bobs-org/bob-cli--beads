# Bead: bob-cli-7n.3 — Two-direction lexer, Markdown guards, and capture-parse wire

[Bead Pages](../README.md) / [bob-cli-7n](README.md) / bob-cli-7n.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.4g.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.4g.linker.w1.md) · **Assignee:** `bob-cli-7n.3` · **Size:** medium
**Created:** 2026-10-14 11:27:20 EDT · **Closed:** 2026-10-14 12:22:24 EDT
**Plan:** [202610/capture\_star\_blocks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_star_blocks.md)

## Description

parse: generalize the `&` scanner to a Blocks direction with the `*` Markdown guards, carry blocked_tasks[] through the execution and editor models, add spans and the blocked_task need, mirror every `&` rejection, and fix the leading-run bug bob-cli-7m.

## Notes

[2026-10-14T16:22:24Z · bob-cli-7n.3--1] Implemented blocked-task capture parsing and wire output; just fmt and just check passed, including the parser and dependency coverage.

## Dependencies

- **Depends on:** [bob-cli-7n.1](bob-cli-7n.1.md) ✓ · ⧖ 2026-10-14
- **Blocks:** [bob-cli-7n.5](bob-cli-7n.5.md) ✓ · ⧖ 2026-10-14
- **Blocks:** [bob-cli-7n.6](bob-cli-7n.6.md) ◐ · ⧖ 2026-10-14

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-7n.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-7n.3.md) | [bob-cli-7n.3](bob-cli-7n.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8774e89`](https://github.com/bobs-org/bob-cli/commit/8774e89f0e4fd0d77793699711b57c7f0c38befe) | feat(capture): parse blocked task capture links | [bob-cli-7n.3](bob-cli-7n.3.md) | 2026-10-14 12:23:01 EDT |
