# Bead: bob-cli-nu.4 — Inline command chips in Live Preview and Reading view

[Bead Pages](../README.md) / [bob-cli-nu](README.md) / bob-cli-nu.4

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5k.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5k.linker.w0.md) · **Assignee:** `bob-cli-nu.4` · **Size:** large
**Created:** 2026-11-20 05:59:33 EST
**Plan:** [202611/command\_chips.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/command_chips.md)

## Description

inline: render run: spans as ▶ pills in Live Preview and Reading view. Click runs through runText and Shift+Click opens Command Mode. Live state comes from a store keyed by signature. Unavailable and copy-only faces cover no-run folders, mobile, and a missing Command Mode. Includes visual previews, perf, and stub-bob e2e.

## Notes

[2026-11-20T12:35:35Z · bob-cli-nu.4] Planning audit: dependency work is landed in bob-plugins at c8da83f (grammar) and 591998e (engine); inline rendering/store/activation is still absent. The landed engine lacks the planned rich resolver metadata, per-run onState callback, and signature-form activeRun contract, so the validated command_chips_inline child epic splits completion into five medium phases: engine-contract, runtime, live, reading, evidence. The child epic land agent owns final verification and closure of nu.4 only; nu remains owned by its land agent. No product or memory files changed in this planning turn. epic-symbols currently reports no entries for nu.4.

## Dependencies

- **Depends on:** [bob-cli-nu.2](bob-cli-nu.2.md) ✓ · ⧖ 2026-11-20
- **Depends on:** [bob-cli-nu.3](bob-cli-nu.3.md) ✓ · ⧖ 2026-11-20
- **Blocks:** [bob-cli-nu.5](bob-cli-nu.5.md) ◐ · ⧖ 2026-11-20
- **Blocks:** [bob-cli-nu.6](bob-cli-nu.6.md) ◐ · ⧖ 2026-11-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-nu.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-nu.4.md) | [bob-cli-nu.4](bob-cli-nu.4.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-nu.3][1] | Check whether the inline phase agent is concurrently editing bob-chips | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.3/README.md

<!-- sase:referenced-by:end -->
