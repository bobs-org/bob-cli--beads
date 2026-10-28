# Bead: bob-cli-dp.2 — Clear the 27 pre-existing Clippy errors on the collision-policy base

[Bead Pages](../README.md) / [bob-cli-dp](README.md) / bob-cli-dp.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-df.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.land.md) · **Assignee:** `bob-cli-dp.2` · **Size:** medium
**Created:** 2026-10-28 11:23:29 EDT · **Closed:** 2026-10-28 11:52:44 EDT
**Plan:** [202610/backlog\_batch\_b5.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch_b5.md)

## Description

core-clippy-cleanup: resolve bob-cli-dh in gh:sase-org/sase-core by reproducing via sase tool run check in an opened core checkout, recording toolchain and exact diagnostics, repairing only still-present violations (agent_hold, bead/cli/tests, bead/touch_index, macro_catalog/tests, artifact_ref_commit_budget, gateway/push, macro_lsp tests), and verifying with sase tool run check. Do not run check-full. Close as superseded with evidence if the current toolchain no longer reproduces.

## Notes

[2026-10-28T15:52:11Z · bob-cli-dp.2] REPRODUCED at clean core HEAD 65546fd2. ToolRun 46ba13dea30f64e140c7e8877a03e284 used rustc 1.99.1 (58cf8f9c3, 2026-10-13) and cargo 1.99.1; Clippy -D warnings rejected std::env::set_var/remove_var (clippy::disallowed_methods): 27 core lib-test diagnostics in agent_hold (2), bead/cli/tests/parsing.rs (9), bead/touch_index.rs (2), macro_catalog/tests/catalog_sources.rs (14); additional targets reported artifact_ref_commit_budget.rs (4), gateway/push.rs (2), macro LSP tests (20 across all targets), and core_py agent_holds/tests.rs (2). Exact locations/output retained in ToolRuns 46ba13dea30f64e140c7e8877a03e284, 734fc992450e94afebdcdaa4e8e67fcd, 3b5ca74dd2e7ec74a7aae00921283c8c, and a1a04aa7d44e17653dcb9387a8718271.

[2026-10-28T15:52:44Z · bob-cli-dp.2] Reproduced the baseline Clippy failures at core HEAD 65546fd2 with rustc 1.99.1 and cargo 1.99.1; replaced shared process environment mutations with thread-local test overrides across core, Python bindings, gateway, and macro LSP tests. `just fmt` passed and `sase tool run check` passed (ToolRun a1a04aa7d44e17653dcb9387a8718271, exit 0, 8m39s). Re-ran `sase bead epic-symbols bob-cli-dp.2`: no remaining symbols.

[2026-10-28T16:02:59Z · bob-cli-dp.2] Recovery turn: Clippy env-guard edits are still dirty in the opened sase-core checkout (21 paths, including untracked crates/sase_core/src/native). Prior ToolRun a1a04aa7d44e17653dcb9387a8718271 passed on this dirty tree (exit 0, 8m39s). Landing the core commit; bead already closed.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-dp.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-dp.2.md) | [bob-cli-dp.2](bob-cli-dp.2.md) | 0 |
