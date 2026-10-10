# Bead: bob-cli-66.5 — Agenda view, row measurer, panel integration, and fixed eye line

[Bead Pages](../README.md) / [bob-cli-66](README.md) / bob-cli-66.5

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.48.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.48.linker.w0.md) · **Assignee:** `bob-cli-66.5` · **Size:** medium
**Created:** 2026-10-09 17:42:23 EDT
**Plan:** [202610/idle\_capture\_pomodoro\_agenda.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/idle_capture_pomodoro_agenda.md)

## Description

mac-agenda-view: build `CaptureAgendaView` and its row views, the offscreen `CaptureAgendaRowMeasurer`, model wiring (visibility, plan, expansions, settle while hidden), auxiliary-region integration with a height cap, fixed eye-line placement instead of re-centring, and the Settings toggle. Add height-consistency and rendered design tests, checked from the CI artifact.

## Notes

[2026-10-10T00:05:43Z · bob-cli-66.5] Committed 27c0c2d to bob-mac-capture master (kept open): CaptureAgendaView + row views, CaptureAgendaRowMeasurer, model wiring, auxiliary integration with budget cap, CapturePanelPlacement eye line, agendaEnabled toggle. CI run https://github.com/bobs-org/bob-cli--beads/actions/runs/38007392441 pending; PNG review + fix-forward owned by monitor follow-up.

## Dependencies

- **Depends on:** [bob-cli-66.3](bob-cli-66.3.md) ✓ · ⧖ 2026-10-09
- **Depends on:** [bob-cli-66.4](bob-cli-66.4.md) ✓ · ⧖ 2026-10-09
- **Blocks:** [bob-cli-66.6](bob-cli-66.6.md) ◐ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-66.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-66.5.md) | [bob-cli-66.5](bob-cli-66.5.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@27c0c2d`](https://github.com/bobs-org/bob-mac-capture/commit/27c0c2d15c721385b7f50805fca22ba75ff44dc9) | feat(agenda): agenda view, row measurer, panel integration, fixed eye line | [bob-cli-66.5](bob-cli-66.5.md) | 2026-10-09 20:03:55 EDT |
| bob-mac-capture | [`bob-mac-capture@c71fe51`](https://github.com/bobs-org/bob-mac-capture/commit/c71fe512c8994dd9bd11e4e1f7483ba95f890c70) | fix(agenda): repair mac-agenda-view CI build errors | [bob-cli-66.5](bob-cli-66.5.md) | 2026-10-09 20:15:26 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-66.3][1] | Check blocked phase scope | 1 |
| read-by | [agent:bob-cli-66.5][2] | Need phase notes and remaining work | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-66.3.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-66.5.md

<!-- sase:referenced-by:end -->
