# Bead: bob-cli-6l.3 — The bob stats command

[Bead Pages](../README.md) / [bob-cli-6l](README.md) / bob-cli-6l.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.0u.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.0u.linker.w0/README.md) · **Assignee:** `bob-cli-6l.3` · **Size:** medium
**Created:** 2026-10-11 07:01:05 EDT · **Closed:** 2026-10-11 13:35:40 EDT
**Plan:** [202610/daily\_stats.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/daily_stats.md)

## Description

cli: register bob stats (overview default, show, metrics) in Daily workflow with human, json, and csv output, the colored terminal glance and detail charts, help/completion/README wiring, and real-vault parity tests.

## Notes

[2026-10-11T17:35:20Z · bob-cli-6l.3] PROPOSED FOLLOW-UP: cli tests capture::r#ref::percent_listen_reference_runs_existing_worker_and_installs_audio and failed_percent_listen_worker_keeps_listen_retry_guidance fail on this tree and identically on clean base; already tracked by bob-cli-6m.

[2026-10-11T17:35:26Z · bob-cli-6l.3] PROPOSED FOLLOW-UP: release CLI on live vault is ~380–420 ms (overview 420, show worked -c 380, metrics 390), still over the 300 ms budget; engine was 365–378 ms; rollout bob-cli-6l.6 owns re-budget.

[2026-10-11T17:35:40Z · bob-cli-6l.3] bob stats (overview default, show, metrics) is in Daily after ready with human/json/csv, colored glance/detail charts, help/completion/README/docs. just fmt+clippy pass. cargo test --lib native::stats: 90 ok. CLI stats+help+completion: 17 ok. just check cargo test failed only on pre-existing capture::r#ref percent-listen (bob-cli-6m; identical on clean base). Release bob stats -f json | jq .ok = true on ~/bob; times recorded in docs/stats.md (overview 420 ms, show worked -c 380 ms, metrics 390 ms). No leftover --epic-symbol entries.

## Dependencies

- **Depends on:** [bob-cli-6l.2](bob-cli-6l.2.md) ✓ · ⧖ 2026-10-11
- **Blocks:** [bob-cli-6l.4](bob-cli-6l.4.md) ◐ · ⧖ 2026-10-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6l.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6l.3/README.md) | [bob-cli-6l.3](bob-cli-6l.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`9be32d9`](https://github.com/bobs-org/bob-cli/commit/9be32d97e56a552d0ef1dc19f3b8eff94ce43638) | feat(stats): add the bob stats CLI (overview, show, metrics) | [bob-cli-6l.3](bob-cli-6l.3.md) | 2026-10-11 13:48:19 EDT |
