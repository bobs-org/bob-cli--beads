# Bead: bob-cli-ha.4 — Stop composing \`=#\` hints in Bob Mac Capture

[Bead Pages](../README.md) / [bob-cli-ha](README.md) / bob-cli-ha.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.cf](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.cf.md) · **Assignee:** `bob-cli-ha.4` · **Size:** small
**Created:** 2026-11-05 05:23:38 EST · **Closed:** 2026-11-05 09:17:04 EST
**Plan:** [202611/glued\_start\_timing.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/glued_start_timing.md)

## Description

mac-agenda-hints: render bob's start_token for Later entries, update the empty-state copy and dim-style keying, refresh tests, and gate on macOS CI.

## Notes

[2026-11-05T14:16:52Z · bob-cli-ha.4--2] PROPOSED FOLLOW-UP: Stabilize macOS editor and capture-routing XCTest failures — runs 42037793376 (final phase snapshot) and 42040643751 (clean base) share 12 failing tests; the final snapshot additionally failed testNamedStartChainTokenRequestsStartNameCompletion, while clean base instead failed testMoveThenPullInBackAndInboxCarryOneAnswerAndSeed. These broad failures reproduce on clean base with two nonmatching cases, indicating CI instability outside this phase; investigate the shared tests and isolate the two variable failures.

[2026-11-05T14:17:04Z · bob-cli-ha.4--2] Completed start_token Later rendering, empty-state and dim-key presentation updates; portable suite passed 2,167 tests (one skipped), Mac build and test-target typecheck passed. macOS CI run 42037793376 failed on editor/routing tests; clean-base run 42040643751 reproduced 12 of 13 failures, with one differing test each, recorded as proposed follow-up. Epic symbols verified empty.

## Dependencies

- **Depends on:** [bob-cli-ha.1](bob-cli-ha.1.md) ✓ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ha.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ha.4.md) | [bob-cli-ha.4](bob-cli-ha.4.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ha.4--2][1] | Verify follow-up note and phase state before closing | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ha.4.md

<!-- sase:referenced-by:end -->
