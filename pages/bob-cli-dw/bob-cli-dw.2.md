# Bead: bob-cli-dw.2 — Make the LSP store identity-lock wait test contend deterministically

[Bead Pages](../README.md) / [bob-cli-dw](README.md) / bob-cli-dw.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-dp.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-dp.land.md) · **Assignee:** `bob-cli-dw.2` · **Size:** small
**Created:** 2026-10-28 15:35:24 EDT · **Closed:** 2026-10-28 15:55:10 EDT
**Plan:** [202610/backlog\_batch\_b6.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch_b6.md)

## Description

lsp-store-lock-flake: resolve bob-cli-dv in sase tests/test_sase_core_wheel_cache_tool.py::test_lsp_store_rechecks_after_waiting_for_identity_lock. The node failed under parallel scoped load of SASE check 5d1634e22bc172fe358db97b9279961f (AssertionError: Waiting for the shared build lock in empty stderr) and passed 3/3 isolated reruns on the same tree (d79366e7627ad5290e34d797cb5c6a7a, f02021819c78b654a26d3739e330ddeb, 6d94f3e4d28d96bbaf830bde9189b048). Root cause: FAKE_CARGO_DELAY=0.3 plus a 5s marker poll lets the first fake cargo finish before the second store contends. Hold the first process in cargo until the second is observed, or otherwise make the lock wait deterministic. Do not suppress the node. Verify with focused serial and parallel reruns plus sase tool run check.

## Notes

[2026-10-28T19:54:58Z · bob-cli-dw.2] PROPOSED FOLLOW-UP: sase tool run check 17abb6ac1c88a765f54da30f7a710db5 failed lint(symvision) on _RecoveryAssessment private import — identical on clean sase master via just _lint-symvision; already tracked as bob-cli-dt / phase bob-cli-dw.1

[2026-10-28T19:55:10Z · bob-cli-dw.2] Handshake holds first fake cargo until the second store prints Waiting for the shared build lock. Node passed 3/3 serial, 8/8 concurrent, and 2/2 xdist-8 file runs. sase tool run check 17abb6ac1c88a765f54da30f7a710db5 failed only the pre-existing _RecoveryAssessment lint (bob-cli-dt), reproduced on clean master; no --epic-symbol leftovers.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-dw.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-dw.2/README.md) | [bob-cli-dw.2](bob-cli-dw.2.md) | 0 |
