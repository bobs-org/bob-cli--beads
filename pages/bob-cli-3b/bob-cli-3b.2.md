# Bead: bob-cli-3b.2 — Roll out NEW and ROTTEN views, badges, docs, and decisions

[Bead Pages](../README.md) / [bob-cli-3b](README.md) / bob-cli-3b.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0uy](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0uy.md) · **Assignee:** `bob-cli-3b.2` · **Size:** medium
**Created:** 2026-10-01 13:09:36 EDT · **Closed:** 2026-10-01 14:04:07 EDT
**Plan:** [202610/freshness\_gated\_ready.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/freshness_gated_ready.md)

## Description

dash-gating: add NEW between TODAY and PENDING, gate READY, rename freshness.md to rotten.md with RETURNED and ROTTEN groups, migrate links and badges, and publish the authorized decision/glossary updates. Deploy the plugin and vault changes together and verify the actual rendered views. Follow the dash-gating section below, including the two-week trial and rollout checks.

## Notes

[2026-10-01T18:03:51Z · bob-cli-3b.2] PROPOSED FOLLOW-UP: capture_pomodoros missing_note_and_missing_section test fails under full-suite parallelism (passes in isolation and identically on clean base; same pattern as 3b.1 flaky capture_complete note)

[2026-10-01T18:03:56Z · bob-cli-3b.2] PROPOSED FOLLOW-UP: live deploy plus Obsidian verification remains: push vault f7d7a2c9, bob plugins sync --no-pull --repo <opened-bob-plugins> --plugin bob-ledger-tools (dry-run first), bob vault-sync to ~/bob, then on athena/apollo/Mac check chips have text, nav/hover/keyboard links, fresh marks survive, Alt+F on rotten source moves to READY, NEW review moves to READY, day rollover updates without hooks/writes, rerender timing, and only then close bob_gtd ^hide-rotten-tasks plus ^scheduled-are-stale (S11 covered in Rust tests) and run the 2026-10-05 through 2026-10-18 trial

[2026-10-01T18:04:07Z · bob-cli-3b.2] Dash-gating landed in 3 commits (bob-cli 286ff35 docs/trial/decisions, bob-plugins d5c1281 rotten fallback 1.12.0, vault f7d7a2c9 NEW/gated-READY/rotten.md/chores/blocked). Verified: cargo fmt ok, clippy ok (exit 0, pre-existing warnings only), freshness-focused cargo tests 22/22, CLI integration 701/701, plugin npm test 1078/1078 plus manifest validate 6/6, dataviewjs syntax OK in dash/rotten, freshness JSON cross-check schema 1 (new 1/rotten 199 buckets match states), hooks dry-run identical before/after (no induced rewrites), vault diff has zero task-byte changes beyond intended chore text. Known gaps recorded as follow-ups: 1 pre-existing parallel-only lib flake (identical on clean base, passes isolated) and the live deploy plus Obsidian rendered-verification gate (push/sync, chip/nav/marks/Alt+F/rollover/timing, vault task closes, 14-day trial execution).

## Dependencies

- **Depends on:** [bob-cli-3b.1](bob-cli-3b.1.md) ✓ · ⧖ 2026-10-01
- **Blocks:** [bob-cli-3b.3](bob-cli-3b.3.md) ✓ · ⧖ 2026-10-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3b.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3b.2/README.md) | [bob-cli-3b.2](bob-cli-3b.2.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`286ff35`](https://github.com/bobs-org/bob-cli/commit/286ff357189e6fbd40016eda5cd643df779f0beb) | docs(freshness,plan): land dash-gating rollout docs, trial, and decisions | [bob-cli-3b.2](bob-cli-3b.2.md) | 2026-10-01 14:02:14 EDT |
| bob-plugins | [`bob-plugins@d5c1281`](https://github.com/bobs-org/bob-plugins/commit/d5c128188ee52ee240b4910b8d7d6429bac84f6b) | feat(ledger-tools): switch status-bar fallback to rotten for dash-gating | [bob-cli-3b.2](bob-cli-3b.2.md) | 2026-10-01 14:02:48 EDT |
