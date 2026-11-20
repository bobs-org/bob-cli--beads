# Bead: bob-cli-nu.4 — Inline command chips in Live Preview and Reading view

[Bead Pages](../README.md) / [bob-cli-nu](README.md) / bob-cli-nu.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5k.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5k.linker.w0.md) · **Assignee:** `bob-cli-nu.4` · **Size:** large
**Created:** 2026-11-20 05:59:33 EST · **Closed:** 2026-11-20 10:59:35 EST
**Plan:** [202611/command\_chips.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/command_chips.md)

## Description

inline: render run: spans as ▶ pills in Live Preview and Reading view. Click runs through runText and Shift+Click opens Command Mode. Live state comes from a store keyed by signature. Unavailable and copy-only faces cover no-run folders, mobile, and a missing Command Mode. Includes visual previews, perf, and stub-bob e2e.

## Notes

[2026-11-20T12:35:35Z · bob-cli-nu.4] Planning audit: dependency work is landed in bob-plugins at c8da83f (grammar) and 591998e (engine); inline rendering/store/activation is still absent. The landed engine lacks the planned rich resolver metadata, per-run onState callback, and signature-form activeRun contract, so the validated command_chips_inline child epic splits completion into five medium phases: engine-contract, runtime, live, reading, evidence. The child epic land agent owns final verification and closure of nu.4 only; nu remains owned by its land agent. No product or memory files changed in this planning turn. epic-symbols currently reports no entries for nu.4.

[2026-11-20T16:00:02Z · bob-cli-nu.4.1.land] bob-cli-nu.4.1 land agent: closing child epic nu.4.1 auto-closed this phase ('delegated work landed'). Verified that the child plan completed every item of the parent plan's 'Phase: inline' (command_chips.md steps 1-7). Rendering: Live Preview gets one chipScanLine pass for both kinds; Reading, embeds, hover, and Tasks/Dataview results get real buttons. Also verified: the commandChipActivate run path, CommandChipRunStore with armed target, every face plus Loading, query-source attribution checked against Tasks 8.6.0 and Dataview 0.5.68, DOM/latch/rebuild/perf tests, stub-bob e2e 23/23 on athena, preview PNGs, and the docs/bob-chips.md 'Command chips' section. Deployed: bob-chips 0.11.0 and bob-command-mode 0.4.0 synced. Shared hooks for nu.5 (fence) and nu.6 (keymap) are exported and not implemented here. Full verification is in the nu.4.1 close note.

## Dependencies

- **Depends on:** [bob-cli-nu.2](bob-cli-nu.2.md) ✓ · ⧖ 2026-11-20
- **Depends on:** [bob-cli-nu.3](bob-cli-nu.3.md) ✓ · ⧖ 2026-11-20
- **Blocks:** [bob-cli-nu.5](bob-cli-nu.5.md) ✓ · ⧖ 2026-11-20
- **Blocks:** [bob-cli-nu.6](bob-cli-nu.6.md) ✓ · ⧖ 2026-11-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-nu.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-nu.4.md) | [bob-cli-nu.4](bob-cli-nu.4.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-nu.3][1] | Check whether the inline phase agent is concurrently editing bob-chips | 1 |
| read-by | [agent:bob-cli-nu.4.1.land][2] | Need the parent phase scope and notes to verify the child epic completed it | 2 |
| read-by | [agent:bob-cli-nu.5][3] | Need sibling phase notes for fence phase context | 1 |
| read-by | [agent:bob-cli-nu.6][4] | See what inline phase landed and any notes relevant to keymap | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.4.1.land/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.5/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.6/README.md

<!-- sase:referenced-by:end -->
