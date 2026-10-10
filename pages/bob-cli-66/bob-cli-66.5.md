# Bead: bob-cli-66.5 — Agenda view, row measurer, panel integration, and fixed eye line

[Bead Pages](../README.md) / [bob-cli-66](README.md) / bob-cli-66.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.48.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.48.linker.w0.md) · **Assignee:** `bob-cli-66.5` · **Size:** medium
**Created:** 2026-10-09 17:42:23 EDT · **Closed:** 2026-10-09 21:06:01 EDT
**Plan:** [202610/idle\_capture\_pomodoro\_agenda.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/idle_capture_pomodoro_agenda.md)

## Description

mac-agenda-view: build `CaptureAgendaView` and its row views, the offscreen `CaptureAgendaRowMeasurer`, model wiring (visibility, plan, expansions, settle while hidden), auxiliary-region integration with a height cap, fixed eye-line placement instead of re-centring, and the Settings toggle. Add height-consistency and rendered design tests, checked from the CI artifact.

## Notes

[2026-10-10T00:05:43Z · bob-cli-66.5] Committed 27c0c2d to bob-mac-capture master (kept open): CaptureAgendaView + row views, CaptureAgendaRowMeasurer, model wiring, auxiliary integration with budget cap, CapturePanelPlacement eye line, agendaEnabled toggle. CI run https://github.com/bobs-org/bob-cli--beads/actions/runs/38007392441 pending; PNG review + fix-forward owned by monitor follow-up.

[2026-10-10T01:05:49Z · bob-cli-66.5--4] PROPOSED FOLLOW-UP: macOS CI timing flakes on degraded arm64 runners (GitHub capacity-constraint annotation on every run) — RefsLibraryTests/testTriggersDuringRefreshRunExactlyOneFollowUp coalescing count, CapturePanelModelTests/testStartPendingListPreviewsTrimmedDraftWithStartDisabled preview waitUntil timeout, RefsPanelModelTests/testRefreshReordersFromNewDataKeepingSelection model timeout; three runs on identical SHA c4dc4b6 fail differently each time while all agenda suites pass; implicated code is byte-identical to green base 3d36a02. Consider bumping waitUntil timeouts or quarantining these tests.

[2026-10-10T01:05:52Z · bob-cli-66.5--4] PROPOSED FOLLOW-UP: epic DECISIONS authorize one decisions-memory record for the idle agenda caching/folding/eye-line policy, but this session has no /sase_memory_write skill available, so the record was not written; land agent should add it via the proper skill.

[2026-10-10T01:06:01Z · bob-cli-66.5--4] CI run https://github.com/bobs-org/bob-mac-capture/actions/runs/38010286522 @ c4dc4b6: Build+Lint green on all 3 attempts; every agenda suite green (Design, FitPlanner, HeightConsistency, InlineText, Model, Models, Presentation, RefreshFilter, RefreshState, Store, Visibility, EyeLine, Placement). Reviewed all agenda-*.png render-fixtures against plan section 6 (thinMaterial pane, title row, pink Now rail+wash, typography, chips, folding ladder, quiet states) — calm and deliberate, no fixes needed. Red only from timing flakes outside phase scope (recorded as PROPOSED FOLLOW-UPs): implicated code byte-identical to green base 3d36a02, failures vary across identical-SHA runs, GitHub flags degraded macOS arm64 capacity. epic-symbols empty.

## Dependencies

- **Depends on:** [bob-cli-66.3](bob-cli-66.3.md) ✓ · ⧖ 2026-10-09
- **Depends on:** [bob-cli-66.4](bob-cli-66.4.md) ✓ · ⧖ 2026-10-09
- **Blocks:** [bob-cli-66.6](bob-cli-66.6.md) ◐ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-66.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-66.5.md) | [bob-cli-66.5](bob-cli-66.5.md) | 4 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@27c0c2d`](https://github.com/bobs-org/bob-mac-capture/commit/27c0c2d15c721385b7f50805fca22ba75ff44dc9) | feat(agenda): agenda view, row measurer, panel integration, fixed eye line | [bob-cli-66.5](bob-cli-66.5.md) | 2026-10-09 20:03:55 EDT |
| bob-mac-capture | [`bob-mac-capture@c71fe51`](https://github.com/bobs-org/bob-mac-capture/commit/c71fe512c8994dd9bd11e4e1f7483ba95f890c70) | fix(agenda): repair mac-agenda-view CI build errors | [bob-cli-66.5](bob-cli-66.5.md) | 2026-10-09 20:15:26 EDT |
| bob-mac-capture | [`bob-mac-capture@c27359f`](https://github.com/bobs-org/bob-mac-capture/commit/c27359ff8e0da4dab3572f752937c08c0c5e20b6) | fix(agenda): repair mac-agenda-view CI test failures | [bob-cli-66.5](bob-cli-66.5.md) | 2026-10-09 20:34:32 EDT |
| bob-mac-capture | [`bob-mac-capture@c4dc4b6`](https://github.com/bobs-org/bob-mac-capture/commit/c4dc4b63062733f73678e33f65c2dc7011a4a025) | fix(agenda): qualify width helper as Self.width in height resolver | [bob-cli-66.5](bob-cli-66.5.md) | 2026-10-09 20:43:40 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-66.3][1] | Check blocked phase scope | 1 |
| read-by | [agent:bob-cli-66.5][2] | Need phase notes and remaining work | 3 |
| read-by | [agent:bob-cli-66.5--1][2] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-66.5--2][2] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-66.5--3][2] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-66.3.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-66.5.md

<!-- sase:referenced-by:end -->
