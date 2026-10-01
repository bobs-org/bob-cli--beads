# Bead: bob-cli-3b.1 — Add cached freshness buckets and matching dashboard models

[Bead Pages](../README.md) / [bob-cli-3b](README.md) / bob-cli-3b.1

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0uy](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0uy.md) · **Assignee:** `bob-cli-3b.1` · **Size:** medium
**Created:** 2026-10-01 13:09:36 EDT
**Plan:** [202610/freshness\_gated\_ready.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/freshness_gated_ready.md)

## Description

ledger-bucket: add the shared read-time bucket contract in bob-ledger-tools and bob-cli, memoize classification and config reads, gate the shared READY count, and implement availability-aware NEW/ROTTEN models and live refresh. Cover the partition, fallback, calendar boundaries, and performance; preserve v1 JSON state names until vocab-rotten. Follow the ledger-bucket section below.

## Notes

[2026-10-01T17:44:16Z · bob-cli-3b.1] PROPOSED FOLLOW-UP: flaky capture_complete day-file-missing test fails under full-suite parallelism (passes in isolation and on re-run)

## Dependencies

- **Blocks:** [bob-cli-3b.2](bob-cli-3b.2.md) ◐ · ⧖ 2026-10-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3b.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3b.1/README.md) | [bob-cli-3b.1](bob-cli-3b.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`6d54e39`](https://github.com/bobs-org/bob-cli/commit/6d54e397bd3ac9acb354b5588748870c8b04d372) | feat(freshness): add read-time buckets, JSON bucket field, and rotten wording | [bob-cli-3b.1](bob-cli-3b.1.md) | 2026-10-01 13:45:47 EDT |
