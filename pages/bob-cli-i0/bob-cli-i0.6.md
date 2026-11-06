# Bead: bob-cli-i0.6 — Earned ETA ranges, plan line, and comparative summary

[Bead Pages](../README.md) / [bob-cli-i0](README.md) / bob-cli-i0.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.199](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.199.md) · **Assignee:** `bob-cli-i0.6` · **Size:** medium
**Created:** 2026-11-06 15:11:24 EST · **Closed:** 2026-11-06 17:26:48 EST
**Plan:** [202611/install\_all\_wait\_and\_whats\_new.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/install_all_wait_and_whats_new.md)

## Description

earned-eta: complete the estimator ladder (p20-p80 range after 5 consistent samples, a bar anchored to the slow end, "taking longer than usual"), add the pre-build plan line and the summary's "about usual" comparison, and replay a compact digest in the summary only when the digest scrolled off.

## Notes

[2026-11-06T22:26:48Z · bob-cli-i0.6] Earned-eta ladder, plan line, summary comparison, and digest replay are in. just check-scripts passed (142 install_ui tests). A sandbox PTY with 6 seeded consistent samples shows the bar, remaining-time range, plan line, and summary comparison; empty history shows only the learning text. Estimator tables cover 0/1/4/5 samples, the 1.6 dispersion gate, A5 outliers, slept/failed/mismatched keys, overtime, monotonic fill, and remaining-time rounding. Plan-line wording, summary clauses, and replay at LINES 24 vs 79 are covered. No leftover --epic-symbol entries.

## Dependencies

- **Depends on:** [bob-cli-i0.5](bob-cli-i0.5.md) ✓ · ⧖ 2026-11-06
- **Blocks:** [bob-cli-i0.7](bob-cli-i0.7.md) ✓ · ⧖ 2026-11-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-i0.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-i0.6/README.md) | [bob-cli-i0.6](bob-cli-i0.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a3238f7`](https://github.com/bobs-org/bob-cli/commit/a3238f70b4582cedb6c2c7fe8f2859d077a783ee) | feat(install): earn ETA ranges, plan line, and summary comparison | [bob-cli-i0.6](bob-cli-i0.6.md) | 2026-11-06 17:28:43 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-i0.6][1] | Confirm assigned bead status and close note before submitting finalizer | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-i0.6/README.md

<!-- sase:referenced-by:end -->
