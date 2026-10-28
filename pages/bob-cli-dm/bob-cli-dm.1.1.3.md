# Bead: bob-cli-dm.1.1.3 — Verify field preservation and publish the contract

[Bead Pages](../README.md) / [bob-cli-dm.1.1](bob-cli-dm.1.1.md) / bob-cli-dm.1.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-dm.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-dm.1.md) · **Assignee:** `bob-cli-dm.1.1.3` · **Size:** medium
**Created:** 2026-10-28 09:05:51 EDT · **Closed:** 2026-10-28 16:50:46 EDT
**Plan:** [202610/task\_theme\_core.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_theme_core.md)

## Description

preservation-contract: test existing task writers, fix field loss, publish the task-theme contract and vault/config references, and run integrated gates.

## Notes

[2026-10-28T20:50:46Z · bob-cli-dm.1.1.3] Preservation contract done. 7 new regressions prove a distinctive authored theme field ((theme::  WRITE) spacing) survives byte-identical: task move (with id repaired to dest), task archive (history line), Highlights checkbox close (completion stamped), ref rename alias overwrite, reconcile set_task_fields (id/dependsOn placed), freshness stamp (theme before fresh/Tasks suffix), closed-task stamp refusal. No writer lost bytes, so no source fixes. Published PT13 in docs/pomodoro-themes.md (PT12 configured-themes anchor preserved; PT1-13 intro updated; suggest added to CLI member list; vectors section lists suggest/task_field/write_rule); theme row + placement in docs/reference/vault-format.md; R1 residence-chain pointer in docs/pomodoro-homes.md; plan.reading_theme in docs/plan.md + docs/reference/configuration.md. just docs-gen clean (no generated drift); just docs-check all gates passed after fixing two anchor slugs (pt13 single-dash; pomodoro-homes same-dir link). Scratch-vault smoke: human existing/new suggest, JSON closed_task with null suggestion, vault byte-identical after queries. Full just check exit 0: 6399 passed, 0 failed. Two full-suite CLI flakes seen along the way (capture completion shell x2, then completion deadline x1) each pass in isolation on this tree and the full CLI suite passed 2373/2373 standalone; pre-existing parallel-suite flakiness, not this diff. Warm-list timing inherited from 1.1.2 closure (41.40 -> 37.08 ms p95, delta -4.32 ms). No epic-symbol entries. No memory, version, or changelog changes; no new beads; ancestors untouched.

## Dependencies

- **Depends on:** [bob-cli-dm.1.1.2](bob-cli-dm.1.1.2.md) ✓ · ⧖ 2026-10-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-dm.1.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-dm.1.1.3/README.md) | [bob-cli-dm.1.1.3](bob-cli-dm.1.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`c624347`](https://github.com/bobs-org/bob-cli/commit/c6243477c4cbc7778cfe4749bb9c6d24a40f2b9e) | feat(themes): publish PT13 pomodoro-theme contract and preservation regressions | [bob-cli-dm.1.1.3](bob-cli-dm.1.1.3.md) | 2026-10-28 16:52:22 EDT |
