# Bead: bob-cli-2b.1 — Pure randomize planner and shared task-field helpers

[Bead Pages](../README.md) / [bob-cli-2b](README.md) / bob-cli-2b.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.2q](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.2q.md) · **Assignee:** `bob-cli-2b.1` · **Size:** medium
**Created:** 2026-09-28 10:45:18 EDT · **Closed:** 2026-09-28 11:12:51 EDT
**Plan:** [202609/bob\_randomize.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/bob_randomize.md)

## Description

planner: lift inline-field parsing into a shared task_fields module; add priority level lookups, seed mixing, the randomize Schedule Log reason and insertion, and hooks helper exposure; build the pure randomize_plan module that turns note snapshots into per-note postimages, a reroll list, skip reasons, and load data. Includes exhaustive unit tests.

## Notes

[2026-09-28T15:12:32Z · bob-cli-2b.1] PROPOSED FOLLOW-UP: clippy deny-by-default overly_complex_bool_expr at tests/cli.rs:30684 fails `just lint` identically on the clean base tree (verified via a detached worktree at HEAD ec31329); unrelated to the planner phase

[2026-09-28T15:12:51Z · bob-cli-2b.1] Planner phase done: task_fields, config lookups/dup-rejection/neutral message/derive_seed, randomize reason+log insertion, hooks visibility+grouping predicate, new randomize_plan with 25 unit tests plus field/reason/config suites. cargo fmt clean, cargo test all green (1024 lib + 556 integration), no new clippy warnings; the one `just lint` failure at tests/cli.rs:30684 reproduces on the clean base tree and is filed as a PROPOSED FOLLOW-UP.

## Dependencies

- **Blocks:** [bob-cli-2b.3](bob-cli-2b.3.md) ◐ · ⧖ 2026-09-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2b.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2b.1/README.md) | [bob-cli-2b.1](bob-cli-2b.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f17339d`](https://github.com/bobs-org/bob-cli/commit/f17339d8117fb10a565f2b8ea9b8e700ee820ec2) | feat(randomize): pure planner phase with shared task-field helpers | [bob-cli-2b.1](bob-cli-2b.1.md) | 2026-09-28 11:14:31 EDT |
