# Bead: bob-cli-dd.2 — Prove FIFO writers and overlapping readers without a wall-clock race

[Bead Pages](../README.md) / [bob-cli-dd](README.md) / bob-cli-dd.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-da.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-da.land.md) · **Assignee:** `bob-cli-dd.2` · **Size:** medium
**Created:** 2026-10-27 18:53:11 EDT · **Closed:** 2026-10-27 19:05:50 EDT
**Plan:** [202610/backlog\_batch\_b3.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch_b3.md)

## Description

command-runner-flake: resolve bob-cli-d9 in bob-plugins with bounded event-based tests for FIFO writers and concurrent readers; preserve production runner policy, run the plugin gates, and sync through bob plugins sync.

## Notes

[2026-10-27T23:05:50Z · bob-cli-dd.2] Replaced wall-clock spawn-gap and 590ms overlap assertions in scripts/test-command-mode-runner.cjs with gated fake-bob lifecycle events. Production runner unchanged (test-only). fake-bob now honors FAKE_BOB_STARTED_FILE / FAKE_BOB_GATE_FILE so the first writer is held until released; the test asserts the second writer does not start while held, starts after the first completes, and preserves FIFO argv order. Both reads must start before either gate is released, then both complete. Failure teardown kills detached children and removes the temp gate dir. Timeouts are deadlock guards only (15s). Verified: focused test 10/10 sequential and 6/6 parallel; whole file 13/13; npm test 3847 pass; npm run validate pass; bob plugins sync --repo <linked bob-plugins> (bob-command-mode up to date). epic-symbols: none. Left bob-cli-d9 open for the lander.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-dd.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-dd.2/README.md) | [bob-cli-dd.2](bob-cli-dd.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@8baf763`](https://github.com/bobs-org/bob-plugins/commit/8baf76398048612cc0ed1c7b7b03537c87056b3b) | test(command-mode): prove writer FIFO and overlapping reads without wall-clock | [bob-cli-dd.2](bob-cli-dd.2.md) | 2026-10-27 19:07:15 EDT |
