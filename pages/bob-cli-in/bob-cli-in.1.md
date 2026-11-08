# Bead: bob-cli-in.1 — Request coordination, failure state, and report counts

[Bead Pages](../README.md) / [bob-cli-in](README.md) / bob-cli-in.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.19v](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.19v.md) · **Assignee:** `bob-cli-in.1` · **Size:** medium
**Created:** 2026-11-08 06:23:52 EST · **Closed:** 2026-11-08 07:16:12 EST
**Plan:** [202611/gmail\_sync\_ii3\_completion.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_sync_ii3_completion.md)

## Description

coordination: make every Gmail read latch auth aborts and give-ups in one injectable coordinator, turn search and preparation failures into a body-free failure state without discarding adoption or recovery, account the -r budget only for waits, and fix the report's membership snapshot and warnings, with unit tests for each.

## Notes

[2026-11-08T12:16:12Z · bob-cli-in.1] CoordinatedRead in retry.rs is the single injectable pace+retry+latch layer for every Gmail read (search, labels, metadata, hydration, policy, attachments). Sticky latches fire from raw inner errors before save/policy re-label: invalid_grant aborts the whole run with a body-free runtime failure and no vault write or journal; wait-budget / retry give-up defers the current candidate and every remaining unprepared key. SharedBudget is wait-only (guard contention, retry backoff, vault-lock waits); ordinary 200ms pacing always applies including at -r 0 and never consumes the budget. Non-auth search failures keep discovered ids, still run adoption/recovery, and report ok=false. Busy vault skip stays quiet exit-0 when prep recorded no failure, and keeps ok=false plus warnings when it did. Report membership uses the apply snapshot when apply ran, else the run's own scan. Fast-forwarded onto origin/master f9601b70 (capture later-start) before close; gmail/sync/guard.rs auto-merged. Verified: cargo test -p bob-obsidian --lib gmail:: (380 passed); cargo test -p bob-obsidian --test gmail_sync --test gmail_shell --test gmail_pull_attach (8+59+2 passed); cargo fmt --all -- --check; just lint. sase bead epic-symbols bob-cli-in.1 reported none.

## Dependencies

- **Blocks:** [bob-cli-in.2](bob-cli-in.2.md) ◐ · ⧖ 2026-11-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-in.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-in.1.md) | [bob-cli-in.1](bob-cli-in.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`3ff3c4f`](https://github.com/bobs-org/bob-cli/commit/3ff3c4fe6c3a45ca52f267702e4e51d5f4e1b2df) | feat(gmail): coordinate every sync Gmail read through one retry layer | [bob-cli-in.1](bob-cli-in.1.md) | 2026-11-08 07:38:41 EST |
