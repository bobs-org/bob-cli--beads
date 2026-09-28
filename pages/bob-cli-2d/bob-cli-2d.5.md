# Bead: bob-cli-2d.5 — list reconciliation view (default subcommand)

[Bead Pages](../README.md) / [bob-cli-2d](README.md) / bob-cli-2d.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.2t](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.2t.md) · **Assignee:** `bob-cli-2d.5` · **Size:** medium
**Created:** 2026-09-28 13:31:29 EDT · **Closed:** 2026-09-28 14:35:44 EDT
**Plan:** [202609/bob\_gkeep\_inbox\_drain.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/bob_gkeep_inbox_drain.md)

## Description

list: implement the two-section Keep/vault reconciliation table with per-note pull states, REF ids, a next-command footer, source filters, `--all`, graceful Keep failure, and `schema_version: 1` JSON, with integration tests.

## Notes

[2026-09-28T18:35:29Z · bob-cli-2d.5] PROPOSED FOLLOW-UP: `cargo clippy --all-targets --all-features` is red on the clean base tree (tests/cli.rs:31818 `overly_complex_bool_expr` deny from `|| true`); fix or remove that clause so `just lint` passes again

[2026-09-28T18:35:44Z · bob-cli-2d.5] Implemented  (default subcommand) in src/native/gkeep/list.rs with two-section table, per-note states, REF ids, footer, -s/-a filters, graceful Keep failure, and schema_version:1 JSON. Added note_counts helper to render.rs. New tests/gkeep_list.rs (11 tests: states, filters, footer variants, duplicates, auth failure, JSON schema, plain pipe output, BOB_NOW ages) plus 2 updated stub assertions in gkeep_cli.rs. Verified: focused suites 17/17 pass, full cargo test green (1116+515+...), fmt clean, clippy clean on lib+list/cli/adapter targets. Pre-existing base-tree clippy deny in tests/cli.rs:31818 recorded as PROPOSED FOLLOW-UP.

## Dependencies

- **Depends on:** [bob-cli-2d.2](bob-cli-2d.2.md) ✓ · ⧖ 2026-09-28
- **Depends on:** [bob-cli-2d.3](bob-cli-2d.3.md) ✓ · ⧖ 2026-09-28
- **Blocks:** [bob-cli-2d.7](bob-cli-2d.7.md) ✓ · ⧖ 2026-09-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2d.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2d.5/README.md) | [bob-cli-2d.5](bob-cli-2d.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`c2a3429`](https://github.com/bobs-org/bob-cli/commit/c2a3429ad1a372caa61a1fb86945ad6ef6ca1d05) | feat(gkeep): implement list reconciliation view (default subcommand) | [bob-cli-2d.5](bob-cli-2d.5.md) | 2026-09-28 14:39:14 EDT |
