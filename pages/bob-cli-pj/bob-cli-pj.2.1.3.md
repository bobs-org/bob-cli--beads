# Bead: bob-cli-pj.2.1.3 — Refresh outside writer locks and prove the complete contract

[Bead Pages](../README.md) / [bob-cli-pj.2.1](bob-cli-pj.2.1.md) / bob-cli-pj.2.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-pj.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-pj.2.md) · **Assignee:** `bob-cli-pj.2.1.3` · **Size:** medium
**Created:** 2026-11-22 18:51:56 EST · **Closed:** 2026-11-22 20:59:25 EST
**Plan:** [202611/refs\_incremental\_coherence.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/refs_incremental_coherence.md)

## Description

lock_refresh_and_contract: carry the refresh budget through lock revalidation, preserve recovery/intake and receipt rules, complete adversarial interleave coverage, document the coherence contract, and run the full repository gates.

## Notes

[2026-11-23T01:59:10Z · bob-cli-pj.2.1.3] PROPOSED FOLLOW-UP: docs-check word budgets over in mac-capture/develop pages — just docs-check fails on base (docs/reference/mac-capture/capture-previews.md 6082>6000, keyboard.md 6036>6000, protocol.md 6107>6000, docs/develop/plugins/plugin-apis.md 8963>8000); none touched by this phase

[2026-11-23T01:59:25Z · bob-cli-pj.2.1.3] Lock-window refresh on shared budget: classify-while-locked/drop-locks/refresh-outside/reacquire loop in scan_apply.rs; recovery+intake consume the one-rebuild allowance (no fresh budget); dest-asset stays locked scan_failed. Tests: 2 new lock-window interleave tests (sidecar subset=locked=0 count=1; daily finalization-only=1 plan line), churn test drives all 4 refreshes+1 rebuild (6 plan lines, inputs_changed, no receipt). Gates: cargo fmt clean, just lint exit 0, workspace tests 12798 passed/0 failed, epic-symbols clean. docs-check fails only on pre-existing word budgets in untouched pages (recorded as follow-up).

## Dependencies

- **Depends on:** [bob-cli-pj.2.1.2](bob-cli-pj.2.1.2.md) ✓ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-pj.2.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-pj.2.1.3/README.md) | [bob-cli-pj.2.1.3](bob-cli-pj.2.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`29d7fec`](https://github.com/bobs-org/bob-cli/commit/29d7fec797ccc09ae932d51cc8a08bf365a637fa) | feat(highlights-ref): lock-window scan coherence with typed ScanChange classification | [bob-cli-pj.2.1.3](bob-cli-pj.2.1.3.md) | 2026-11-22 21:00:28 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pj.2.1.3][1] | check phase notes and remaining work | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-pj.2.1.3/README.md

<!-- sase:referenced-by:end -->
