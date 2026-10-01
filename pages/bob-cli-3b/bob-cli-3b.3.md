# Bead: bob-cli-3b.3 — Finish the rotten vocabulary and versioned contract migration

[Bead Pages](../README.md) / [bob-cli-3b](README.md) / bob-cli-3b.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0uy](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0uy.md) · **Assignee:** `bob-cli-3b.3` · **Size:** medium
**Created:** 2026-10-01 13:09:36 EDT · **Closed:** 2026-10-01 14:27:13 EDT
**Plan:** [202610/freshness\_gated\_ready.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/freshness_gated_ready.md)

## Description

vocab-rotten: rename freshness-specific machine state/count/config names in Rust and JavaScript, publish bob freshness JSON schema 2, and support the old budget key with a deprecation lint for one release. Update every freshness consumer and conformance test, preserve the bucket contract and unrelated stale terminology, then release and verify the final integration. Follow the vocab-rotten section below.

## Notes

[2026-10-01T18:26:45Z · bob-cli-3b.3] PROPOSED FOLLOW-UP: capture_pomodoros missing-note test flakes under parallel runs via unsynchronized with_env process-env mutation (fails identically on clean base; passes alone)

[2026-10-01T18:26:53Z · bob-cli-3b.3] PROPOSED FOLLOW-UP: this-machine ~/bob vault still on plugin 1.9.0 + freshness.md/REVIEW (dash-gating vault rollout not yet synced here); needs coordinated vault-sync and Obsidian live verification of NEW/ROTTEN views after the 1.13.0/1.49.0 plugin sync

[2026-10-01T18:27:13Z · bob-cli-3b.3] vocab-rotten done: FreshState::Rotten, Counts.rotten, rotten_daily_budget with one-release legacy key + once-per-config deprecation lint, JSON schema 2, JS namespace v3 (ledger-tools 1.13.0, nav-hotkeys 1.49.0). Verified: cargo fmt/clippy/test (56 unit + 25 CLI incl. 3 new legacy tests), npm test 1078/1078, manifest validate 6/6, deployed binary reports schema 2 with rotten keys + single deprecation warning, plugins synced with backups. One pre-existing parallel flake (capture_pomodoros env race, fails on base too) recorded as follow-up.

## Dependencies

- **Depends on:** [bob-cli-3b.2](bob-cli-3b.2.md) ✓ · ⧖ 2026-10-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3b.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3b.3/README.md) | [bob-cli-3b.3](bob-cli-3b.3.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e77bbe3`](https://github.com/bobs-org/bob-cli/commit/e77bbe387ae4a88521a86b962bbb7fb8ae75e469) | feat(freshness): finish rotten vocabulary and versioned contract migration | [bob-cli-3b.3](bob-cli-3b.3.md) | 2026-10-01 14:29:46 EDT |
| bob-plugins | [`bob-plugins@3cb3016`](https://github.com/bobs-org/bob-plugins/commit/3cb301606491a1a111e5d99a8e85c8b217ba39be) | feat(ledger-tools): rename freshness state to rotten, namespace v3, one-release legacy budget key | [bob-cli-3b.3](bob-cli-3b.3.md) | 2026-10-01 14:30:15 EDT |
