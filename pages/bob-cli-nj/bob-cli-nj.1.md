# Bead: bob-cli-nj.1 — bob-cli: vault-derived log phrase catalog and \`bob logs list\`

[Bead Pages](../README.md) / [bob-cli-nj](README.md) / bob-cli-nj.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.f3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.f3.md) · **Assignee:** `bob-cli-nj.1` · **Size:** medium
**Created:** 2026-11-19 12:14:02 EST · **Closed:** 2026-11-19 14:28:09 EST
**Plan:** [202611/log\_reason\_recall.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/log_reason_recall.md)

## Description

logs-catalog: add a cached scanner over task Schedule, Work, Rotten, and Cancel Logs. It filters out machine-written text using a classifier backed by a writer registry test, then ranks by tiered literal match plus newest-pinned frecency. It ships the read-only `bob logs list` (human and JSON output), the shared rank vectors, and the docs/log-recall.md contract.

## Notes

[2026-11-19T19:23:22Z · bob-cli-nj.1] PROPOSED FOLLOW-UP: Existing task bob-cli-nf tracks the 12 host-date-dependent bob tick CLI failures; just check reported the same 12, and tick::gcal_yesterday_scope_cooldown_and_waiting_status reproduced identically on clean HEAD 5b4c2636 (2026-11-19).

[2026-11-19T19:28:09Z · bob-cli-nj.1] Implemented vault-derived phrase recall and bob logs list. cargo test --lib passed (7,398 passed, 4 ignored); CLI catalog/help snapshot tests passed; just docs-check passed all gates and 448 docs tests; live human and JSON bob logs list smoke checks passed. just check clippy passed, but 12 tick CLI tests remain red exactly as tracked by bob-cli-nf; reproduced the readiness failure on clean HEAD 5b4c2636 and recorded that corroboration.

## Dependencies

- **Blocks:** [bob-cli-nj.2](bob-cli-nj.2.md) ◐ · ⧖ 2026-11-19
- **Blocks:** [bob-cli-nj.5](bob-cli-nj.5.md) ◐ · ⧖ 2026-11-19
- **Blocks:** [bob-cli-nj.6](bob-cli-nj.6.md) ◐ · ⧖ 2026-11-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-nj.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nj.1/README.md) | [bob-cli-nj.1](bob-cli-nj.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`382963d`](https://github.com/bobs-org/bob-cli/commit/382963dbae5ee9a11c5492c1bf9ddb192abd3199) | feat(logs): add vault-derived phrase recall | [bob-cli-nj.1](bob-cli-nj.1.md) | 2026-11-19 14:30:15 EST |
