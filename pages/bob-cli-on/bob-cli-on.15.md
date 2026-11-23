# Bead: bob-cli-on.15 — Requirements on the Mac Pull-In card

[Bead Pages](../README.md) / [bob-cli-on](README.md) / bob-cli-on.15

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1ex](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1ex.md) · **Assignee:** `bob-cli-on.15` · **Size:** large
**Created:** 2026-11-21 11:13:27 EST · **Closed:** 2026-11-22 21:38:26 EST
**Plan:** [202611/task\_requirements.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_requirements.md)

## Description

mac-close-card: decode requirement groups, carry them through every offer path, stage met/drop/carry/pull-in verdicts with overlap feedback, and submit them behind --req-choice in Bob Mac Capture.

## Notes

[2026-11-23T02:38:38Z · bob-cli-on.15.1.land] Verified by bob-cli-on.15.1 land agent before the cascade close: the child epic bob-cli-on.15.1 delivered every mac-close-card item in plan:202611/task_requirements.md: tolerant decoding of pull_in.reqs/groups/req rows/req_outcomes; collection through preview snapshot, refusal refresh, CaptureSuccessorOfferRows, view and NotificationService; Met/Drop+reason/Carry (Ctrl+Shift+T)/Carry-and-pull (Space/Tab)/Ctrl+J pin, branch fold, on-row overlap refusal, mark-all excluding req rows; requirement-first rendering with Bob copy, glyph runs, consequences, footer and accessibility; --req-choice gated submission with Shift-Return downgrade and unchanged Esc; fixtures generated from real bob; Mac keyboard/capture-previews/protocol docs. Mac master c0959905 exact-SHA macOS CI green (run 45098831346); Mac and bob-cli just docs-check pass. Outer epic bob-cli-on left to its own land agent.

## Dependencies

- **Depends on:** [bob-cli-on.14](bob-cli-on.14.md) ✓ · ⧖ 2026-11-21
- **Depends on:** [bob-cli-on.8](bob-cli-on.8.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.15](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.15.md) | [bob-cli-on.15](bob-cli-on.15.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-on.15.1.land][1] | Need the parent link and phase scope to verify the child epic completed it | 2 |
| read-by | [agent:research.5u.cld][2] | Check whether in-flight req card/memory phases render or record the hash run glyph, for display redesign timing | 1 |
| read-by | [agent:research.5u.gem][3] | Inspect display-related and remaining phases of bob-cli-on | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.15.1.land/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.5u.cld/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.5u.gem/README.md

<!-- sase:referenced-by:end -->
