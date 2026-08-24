# Bead: bob-cli-13.1 — Position-free @@ declarations in the capture grammar

[Bead Pages](../README.md) / [bob-cli-13](README.md) / bob-cli-13.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0cv](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.0cv.md) · **Assignee:** `bob-cli-13.1` · **Size:** medium
**Created:** 2026-08-24 15:01:18 EDT · **Closed:** 2026-08-24 15:24:20 EDT
**Plan:** [202608/capture\_global\_destination\_anywhere.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/capture_global_destination_anywhere.md)

## Description

grammar: make any `@@…` token a global destination declaration anywhere in a draft, drop the header-line-only restriction, add duplicate-declaration and shadowed-local diagnostics, and update capture, capture-parse, capture-complete, help text, docs, and tests.

## Notes

[2026-08-24T19:24:20Z · bob-cli-13.1] Implemented position-free @@ global destination declarations for capture grammar, parse, completion, capture warnings, docs, and tests; verified with just.

## Dependencies

- **Blocks:** [bob-cli-13.2](bob-cli-13.2.md) ✓ · ⧖ 2026-08-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-13.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-13.1/README.md) | [bob-cli-13.1](bob-cli-13.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`5b15533`](https://github.com/bobs-org/bob-cli/commit/5b155336ff772fb1f9f3dae6b3579fb8ff7f1f39) | feat(capture): allow global destination declarations anywhere | [bob-cli-13.1](bob-cli-13.1.md) | 2026-08-24 15:25:14 EDT |
