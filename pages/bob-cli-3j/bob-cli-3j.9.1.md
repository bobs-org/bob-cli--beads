# Bead: bob-cli-3j.9.1 — Completion results, bash insertion, and capture-grammar integration

[Bead Pages](../README.md) / [bob-cli-3j.9](bob-cli-3j.9.md) / bob-cli-3j.9.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-3j.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-3j.land.md) · **Assignee:** `bob-cli-3j.9.1` · **Size:** medium
**Created:** 2026-10-02 14:29:07 EDT · **Closed:** 2026-10-02 15:23:56 EDT
**Plan:** [202610/shell\_completion\_landing\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/shell_completion_landing_fixes.md)

## Description

results: make body-bearing @route: follow capture-complete's new-ID intent, honor ValueHints and positional file slots, fix the stale capture-complete TEXT hint, make the bash adapter insert correctly across = wordbreaks, open quotes, spaces, and attached !files-in, and add goldens and docs for the =x/=*/=! capture changes.

## Notes

[2026-10-02T19:23:49Z · bob-cli-3j.9.1] PROPOSED FOLLOW-UP: zsh zpty harness gotcha — `zpty -w pb ""` sends zero bytes (Enter never arrives); send Enter as `zpty -w -n pb $\x27\\r\x27` — relevant to lifecycle-phase zpty tests

[2026-10-02T19:23:56Z · bob-cli-3j.9.1] results phase done: PomodoroBlockId follows capture-complete intent (solo @dev: links, body-bearing suggests new IDs), TEXT hint fixed, ValueHint precedence + PDF output scoped to highlights clip/create, positional value slots, bash adapter strips every wordbreak/handles open quotes/escapes/!files-in, =x/=*/=! goldens + docs. Verified: cargo fmt clean, clippy only pre-existing pomodoro_name:808 deny, cargo test all green (incl. new readline e2e), just install-smoke exit 0

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-3j.9.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-3j.9.1/README.md) | [bob-cli-3j.9.1](bob-cli-3j.9.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`712d277`](https://github.com/bobs-org/bob-cli/commit/712d27773fcb4b207887a3b7f332766d2e5f60e8) | feat(completion): body-bearing @route, TEXT hints, ValueHints, positional slots, bash adapter | [bob-cli-3j.9.1](bob-cli-3j.9.1.md) | 2026-10-02 15:25:26 EDT |
