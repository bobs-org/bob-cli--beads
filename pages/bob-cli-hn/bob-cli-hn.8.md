# Bead: bob-cli-hn.8 — CaptureCore decoding, outcome model, argv, and fixtures

[Bead Pages](../README.md) / [bob-cli-hn](README.md) / bob-cli-hn.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.191](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.191/README.md) · **Assignee:** `bob-cli-hn.8` · **Size:** medium
**Created:** 2026-11-05 18:41:47 EST · **Closed:** 2026-11-05 22:31:51 EST
**Plan:** [202611/successor\_card\_verdicts.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/successor_card_verdicts.md)

## Description

mac-core: decode the new bob fields and refusals, add the portable CapturePullInOutcomes model, gate `--complete-offer` and `--cancel-offer` argv on pull_in.close, and generate fixtures from a real bob.

## Notes

[2026-11-06T03:31:51Z · bob-cli-hn.8] Implemented CaptureCore offer-close decoding, portable outcomes, capability-gated argv, fake-bob support, and real-Bob fixtures. Verified Bob build and fixture generation; just portable-check passed (2,194 tests, 1 skipped).

## Dependencies

- **Depends on:** [bob-cli-hn.3](bob-cli-hn.3.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hn.9](bob-cli-hn.9.md) ◐ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-hn.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hn.8/README.md) | [bob-cli-hn.8](bob-cli-hn.8.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hn.8][1] | Verify the implemented phase scope before closure | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hn.8/README.md

<!-- sase:referenced-by:end -->
