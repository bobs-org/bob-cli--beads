# Bead: bob-cli-1t.1 — Pomodoro ledger scanner and \`bob capture-pomodoros\`

[Bead Pages](../README.md) / [bob-cli-1t](README.md) / bob-cli-1t.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0fk](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.0fk.md) · **Assignee:** `bob-cli-1t.1` · **Size:** medium
**Created:** 2026-08-28 12:37:06 EDT · **Closed:** 2026-08-28 12:54:10 EDT
**Plan:** [202608/capture\_named\_pomodoro.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/capture_named_pomodoro.md)

## Description

pomodoro_ledger: add the shared named-Pomodoro scanner (name, slug, time range, current, stale-safe ref, selection) and the read-only discovery command that exposes it.

## Notes

[2026-08-28T16:54:10Z · bob-cli-1t.1] Implemented shared selector slug, Pomodoro ledger scanner, capture-pomodoros CLI, docs, smoke entry, and tests. Verified cargo fmt --check, cargo clippy --all-targets --all-features, cargo test, manual BOB_DAY_FILE capture-pomodoros JSON and -a jq smoke; epic-symbols reported no leftovers.

## Dependencies

- **Blocks:** [bob-cli-1t.2](bob-cli-1t.2.md) ✓ · ⧖ 2026-08-28
- **Blocks:** [bob-cli-1t.3](bob-cli-1t.3.md) ✓ · ⧖ 2026-08-28
- **Blocks:** [bob-cli-1t.4](bob-cli-1t.4.md) ✓ · ⧖ 2026-08-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-1t.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-1t.1/README.md) | [bob-cli-1t.1](bob-cli-1t.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`cc4c9a3`](https://github.com/bobs-org/bob-cli/commit/cc4c9a38684e2ed70af7c65df745029a03aa6503) | feat(capture): list pomodoro ledger entries | [bob-cli-1t.1](bob-cli-1t.1.md) | 2026-08-28 12:55:02 EDT |
