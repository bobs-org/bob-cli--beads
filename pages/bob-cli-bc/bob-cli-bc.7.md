# Bead: bob-cli-bc.7 — Mac Capture recent rows, Ctrl+D hide, and Name it suggestions

[Bead Pages](../README.md) / [bob-cli-bc](README.md) / bob-cli-bc.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2c.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2c.linker.w1.md) · **Assignee:** `bob-cli-bc.7` · **Size:** medium
**Created:** 2026-10-24 07:52:22 EDT · **Closed:** 2026-10-24 14:07:01 EDT
**Plan:** [202610/pomodoro\_themes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/pomodoro_themes.md)

## Description

mac-menus: render Today/Recent rows with swatches, hide and undo with Ctrl+D, and suggest themes in the Name it prompt.

## Notes

[2026-10-24T18:06:47Z · bob-cli-bc.7--1] PROPOSED FOLLOW-UP: Repair or triage the clean-base bob-cli just check failures at 2da7bbef. The library test native::completion::kinds::tests::every_value_arg_has_a_decision reports themes rename positional args without completion-kind decisions. CLI failures are capture::related::draft_related_stays_under_the_debug_perf_gate, completion::bash::bash_strips_every_wordbreak_not_just_colon, completion::capture_text::named_start_completes_after_hash, completion::capture_text::named_start_after_inline_close_keeps_prefix, help_options::capture_complete_help_lists_options_alphabetically, and both highlights::continuations tests. The checkout was clean and HEAD equaled origin/master when just check ran, so these failures reproduce on the clean base.

[2026-10-24T18:07:01Z · bob-cli-bc.7--1] Mac bundle and all four typechecked test targets pass; Athena portable-check passes all 1,591 tests. bob-cli just check ran on clean HEAD 2da7bbef, equal to origin/master, and failed one library test plus seven CLI tests; the unchanged failures are recorded in the PROPOSED FOLLOW-UP note. epic-symbols reported no leftovers.

## Dependencies

- **Depends on:** [bob-cli-bc.3](bob-cli-bc.3.md) ✓ · ⧖ 2026-10-24
- **Depends on:** [bob-cli-bc.4](bob-cli-bc.4.md) ✓ · ⧖ 2026-10-24
- **Blocks:** [bob-cli-bc.8](bob-cli-bc.8.md) ✓ · ⧖ 2026-10-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-bc.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-bc.7.md) | [bob-cli-bc.7](bob-cli-bc.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@a49a08b`](https://github.com/bobs-org/bob-mac-capture/commit/a49a08b0c5bfb8ed50baec9424388188583c12e3) | feat(capture): add recent theme menus and name suggestions | [bob-cli-bc.7](bob-cli-bc.7.md) | 2026-10-24 14:11:37 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.2][1] | Identify the existing owner and task evidence for clean-base just check failures | 1 |
| read-by | [agent:bob-cli-bc.7--1][2] | Review the assigned phase and record the clean-base gate result | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-an.6.6.6.5.6.5.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-bc.7.md

<!-- sase:referenced-by:end -->
