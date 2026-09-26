# Bead: bob-cli-26.1 — Capture grammar and atomic Pomodoro start

[Bead Pages](../README.md) / [bob-cli-26](README.md) / bob-cli-26.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.20](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.20/README.md) · **Assignee:** `bob-cli-26.1` · **Size:** medium
**Created:** 2026-09-26 16:50:55 EDT · **Closed:** 2026-09-26 17:06:59 EDT
**Plan:** [202609/capture\_start\_pomodoro.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/capture_start_pomodoro.md)

## Description

capture-core: parse the se-compatible suffix and stage the task, link, and timed ledger entry atomically.

## Notes

[2026-09-26T21:06:59Z · bob-cli-26.1] capture-core done: se<X> start suffix (=, =3, =-, =-2, =3-) with 5-min rounding from BOB_NOW, atomic placeholder start+link via staged snapshot, pomodoro_start JSON, help, 7 integration tests; cargo test lib 898 pass, cli 471 pass, clippy plain pass, fmt clean for touched files

## Dependencies

- **Blocks:** [bob-cli-26.2](bob-cli-26.2.md) ✓ · ⧖ 2026-09-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-26.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-26.1/README.md) | [bob-cli-26.1](bob-cli-26.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a9a3465`](https://github.com/bobs-org/bob-cli/commit/a9a3465326af6b5415a95cf1804081c404f4fdcc) | feat(capture): atomic Pomodoro start via se\<X\> suffix | [bob-cli-26.1](bob-cli-26.1.md) | 2026-09-26 17:08:17 EDT |
