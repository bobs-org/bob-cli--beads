# Bead: bob-cli-on.11.1.6 — Connect managed Done paths and verify the complete card flow

[Bead Pages](../README.md) / [bob-cli-on.11.1](bob-cli-on.11.1.md) / bob-cli-on.11.1.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-on.11](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.11.md) · **Assignee:** `bob-cli-on.11.1.6` · **Size:** medium
**Created:** 2026-11-22 14:59:31 EST · **Closed:** 2026-11-22 19:48:18 EST
**Plan:** [202611/obsidian\_requirement\_close\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/obsidian_requirement_close_card.md)

## Description

close_wiring: capture pre-close scope on all managed Done paths, integrate one requirement-first card and ordered apply, resolve jumps last, finish contract docs, and verify both deployed plugins.

## Notes

[2026-11-23T00:04:24Z · bob-cli-on.11.1.6--1] PROPOSED FOLLOW-UP: Stabilize the existing 25 ms wall-clock timing checks under full-suite load: event-link-times failed at 74.8 ms on clean bob-plugins base 175283d3 (and 26.8 ms on this phase tree), tracked by bob-cli-km; frees-marks failed at 40 ms on that same clean base, tracked by bob-cli-io. These files are unchanged by this phase.

[2026-11-23T00:48:18Z · bob-cli-on.11.1.6--4] Implemented managed Done close wiring across all paths: captures pre-close scope, routes one requirement-first card with ordered apply, resolves jump landings last, and completes the contract docs. `just check` passed in workspace 21. Clean-base timing flakes `event-link-times` and `frees-marks` remain tracked by bob-cli-km and bob-cli-io; neither file was changed by this phase. Deployed and verified bob-navigation-hotkeys 2.107.0 and task-status-cycler 1.58.1 (`bob plugins list` reports both synced); task-status-cycler was synced without force.

## Dependencies

- **Depends on:** [bob-cli-on.11.1.3](bob-cli-on.11.1.3.md) ✓ · ⧖ 2026-11-22
- **Depends on:** [bob-cli-on.11.1.5](bob-cli-on.11.1.5.md) ✓ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.11.1.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.11.1.6.md) | [bob-cli-on.11.1.6](bob-cli-on.11.1.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`c17dd80`](https://github.com/bobs-org/bob-cli/commit/c17dd80a0b238a96c22e293badf82cdd54e4ced8) | docs(requirements): clarify managed Done close card availability | [bob-cli-on.11.1.6](bob-cli-on.11.1.6.md) | 2026-11-22 18:06:50 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-on.11.1.7.2--2][1] | Check the previous phase's evidence for the same full-suite timing flakes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.11.1.7.2.md

<!-- sase:referenced-by:end -->
