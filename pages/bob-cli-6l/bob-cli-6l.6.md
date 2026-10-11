# Bead: bob-cli-6l.6 — Rollout — real-vault verification, docs, and memory

[Bead Pages](../README.md) / [bob-cli-6l](README.md) / bob-cli-6l.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.0u.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.0u.linker.w0/README.md) · **Assignee:** `bob-cli-6l.6` · **Size:** small
**Created:** 2026-10-11 07:01:05 EDT · **Closed:** 2026-10-11 17:00:17 EDT
**Plan:** [202610/daily\_stats.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/daily_stats.md)

## Description

rollout: verify end to end on the live vault and every installed surface, record measured performance, finish docs and README cross-links, apply only the accepted memory decisions, and record follow-ups.

## Notes

[2026-10-11T20:59:59Z · bob-cli-6l.6] PROPOSED FOLLOW-UP: snapshot kind — nightly lane sizes and walk-due-at-start recorded by bob nightly so Stats can chart state the vault forgets

[2026-10-11T21:00:04Z · bob-cli-6l.6] PROPOSED FOLLOW-UP: POST-closeout summary toast — after Morning review closes, show "Review closed · 41 answered · 1h 40m · keep 82%" from that day’s stats

[2026-10-11T21:00:08Z · bob-cli-6l.6] PROPOSED FOLLOW-UP: four-week revisit — keep the metrics that changed a decision, hide the rest, and consider goals only then

[2026-10-11T21:00:13Z · bob-cli-6l.6] PROPOSED FOLLOW-UP: shrink live-vault stats compute toward 300ms — rollout recorded 340–370 ms on apollo ~/bob (HEAD efc5593); original plan target was ≤300 ms

[2026-10-11T21:00:17Z · bob-cli-6l.6] Live vault: release bob stats overview/show/metrics/csv and -f json (.ok true) on apollo ~/bob; gated BOB_STATS_REAL_VAULT_PARITY engine 371ms and CLI 350ms oracles passed; journal writer deployed and gitignore !/.bob/stats/**/*.jsonl trackable, but no .bob/stats/review files yet on apollo/athena/mac (Reviewed not_tracked); vault-sync status clean; plugins synced from linked bob-plugins (ledger-tools 1.47.0); dash_stats.md and STATS chip present. Recorded 340–370ms CLI (re-budget vs ≤300ms). Docs cross-links in README, docs/README, dashboard, vault-git-sync, stats. memory_stats_record/memory_journal_term left untouched. Obsidian GUI not reachable here; page contract is in place for Bryan to open Stats.

[2026-10-11T21:09:15Z · bob-cli-6l.6--1] PROPOSED FOLLOW-UP: cli tests capture::r#ref::percent_listen_reference_runs_existing_worker_and_installs_audio and failed_percent_listen_worker_keeps_listen_retry_guidance fail identically on this tree (listen.log missing / listen runner never invoked); tracked by bob-cli-6m; docs-only phase did not touch capture

## Dependencies

- **Depends on:** [bob-cli-6l.5](bob-cli-6l.5.md) ✓ · ⧖ 2026-10-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6l.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6l.6.md) | [bob-cli-6l.6](bob-cli-6l.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f11ca41`](https://github.com/bobs-org/bob-cli/commit/f11ca415b6fefc329b776be081ee36fd041bcb1d) | docs(stats): cross-link CLI, Stats page, and review journal | [bob-cli-6l.6](bob-cli-6l.6.md) | 2026-10-11 17:13:06 EDT |
