# Bead: bob-cli-oe.4 — task-status-cycler honors the pin after every managed Done

[Bead Pages](../README.md) / [bob-cli-oe](README.md) / bob-cli-oe.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5m.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5m.linker.w0.md) · **Assignee:** `bob-cli-oe.4` · **Size:** medium
**Created:** 2026-11-20 17:03:14 EST · **Closed:** 2026-11-20 18:51:31 EST
**Plan:** [202611/successor\_jump\_pin.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/successor_jump_pin.md)

## Description

cycler-jump-close: offer the pin only when the caller can honor it; keep `jump` through normalization; resolve the target's post-write identity from picks, closes, or recovery edits; land after retirement and the notice, or return it to walk-owned callers. Covers the Vim Ctrl+Enter walk path, parked successors, and cycler API v6.

## Notes

[2026-11-20T23:51:06Z · bob-cli-oe.4--2] PROPOSED FOLLOW-UP: ledger-tools 25ms perf budgets flake under full-suite load — test-ledger-tools-event-link-times (76.2ms vs 25ms budget) and test-ledger-tools-frees-marks (97ms vs 25ms) failed in the full npm-test run (7988/7990 pass), but both pass in isolation on this tree (11.2ms and 23.2ms). plugins/bob-ledger-tools plus both test files are byte-identical to HEAD (git diff --quiet exit 0), so the phase did not cause this; absolute wall-clock budgets plus full-suite load explain it. Consider raising budgets, averaging repeats, or moving these perf asserts to test:perf.

[2026-11-20T23:51:13Z · bob-cli-oe.4--2] PROPOSED FOLLOW-UP: docs:check lint word budgets already over on the clean base tree — docs/develop/plugin-apis.md is 8175 words at HEAD vs the 8000-word develop/ cap (phase adds ~46 words to 8221), and docs/reference/vault-format.md fails its 6000-word cap with a clean primary worktree (untouched by this phase). Both reproduce without phase changes; consider a budget bump or splitting the pages.

[2026-11-20T23:51:31Z · bob-cli-oe.4--2] Verified: docs inventory regenerated (index, task-status-cycler v1.52.0 API section) so docs:inventory:check passes; all task-status-cycler tests pass in the full unit run (7988/7990, only 2 failures are pre-existing ledger-tools 25ms perf flakes that pass in isolation at 11ms/23ms with files byte-identical to HEAD); bob plugins sync deployed (2 copied, 0 skipped). docs:check lint word-budget overages and the perf flakes reproduce on the clean base tree and are recorded as PROPOSED FOLLOW-UP notes on this bead.

## Dependencies

- **Depends on:** [bob-cli-oe.3](bob-cli-oe.3.md) ✓ · ⧖ 2026-11-20
- **Blocks:** [bob-cli-oe.5](bob-cli-oe.5.md) ✓ · ⧖ 2026-11-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-oe.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-oe.4.md) | [bob-cli-oe.4](bob-cli-oe.4.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-oe.4--2][1] | Inspect oe.4 phase scope to judge perf failures | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-oe.4.md

<!-- sase:referenced-by:end -->
