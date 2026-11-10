# Bead: bob-cli-ji.7.1.4 — Mode entry points, capture preservation, and event picker

[Bead Pages](../README.md) / [bob-cli-ji.7.1](bob-cli-ji.7.1.md) / bob-cli-ji.7.1.4

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ji.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ji.7.md) · **Assignee:** `bob-cli-ji.7.1.4` · **Size:** medium
**Created:** 2026-11-10 10:29:45 EST
**Plan:** [202611/mac\_event\_note\_mode.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_event_note_mode.md)

## Description

picker: wire Command-E, Event Note status menu, and Calendar-row URL entry into a surface inside the capture panel with a grouped keyboard picker. Keep the actual capture editor and its undo manager alive; route focus, sizing, Escape, capability, and panel switches without capture writes. Cover the entry and restoration paths in hosted tests. Read Picker and entry.

## Notes

[2026-11-10T19:37:45Z · bob-cli-ji.7.1.4--6] PROPOSED FOLLOW-UP: Pre-existing CaptureAliasTipPanelTests waitUntil timeouts (testFilteringKeepsTheShownTipAnchoredToTheSigil, testOptionTypedHashOpensTheHashTip, testTypingQueryBeforeTheRouteListOpensKeepsTheTip) failed identically on exact-SHA run 42883209970 and base aafed83/6b6052c (runs 42826766066, 42838952067); same class as flake bead bob-cli-jk / bob-cli-ji.7.1.2 follow-up — picker Command-E assertion is the only introduced Test failure

## Dependencies

- **Depends on:** [bob-cli-ji.7.1.2](bob-cli-ji.7.1.2.md) ✓ · ⧖ 2026-11-10
- **Blocks:** [bob-cli-ji.7.1.5](bob-cli-ji.7.1.5.md) ◐ · ⧖ 2026-11-10

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ji.7.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ji.7.1.4.md) | [bob-cli-ji.7.1.4](bob-cli-ji.7.1.4.md) | 3 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@cdd7384`](https://github.com/bobs-org/bob-mac-capture/commit/cdd73844aec701344b2fa8d1be97eb49d30d5ed0) | feat(capture): add Event Note picker overlay in capture panel | [bob-cli-ji.7.1.4](bob-cli-ji.7.1.4.md) | 2026-11-10 13:54:12 EST |
| bob-mac-capture | [`bob-mac-capture@f32a575`](https://github.com/bobs-org/bob-mac-capture/commit/f32a575071d016a8aa4c7e35dceae157d4cb58ba) | fix(capture): import CaptureCore testably in Event Note picker tests | [bob-cli-ji.7.1.4](bob-cli-ji.7.1.4.md) | 2026-11-10 14:10:47 EST |
| bob-mac-capture | [`bob-mac-capture@90b6f9e`](https://github.com/bobs-org/bob-mac-capture/commit/90b6f9e3cd96b3513687e35e85167a75f69578a8) | fix(capture): expect Command-E to open Event Note in the line-motion test | [bob-cli-ji.7.1.4](bob-cli-ji.7.1.4.md) | 2026-11-10 14:40:18 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ji.7.1.4--4][1] | Need the full phase description, DECISIONS, notes, and design file after failed macOS CI | 2 |
| read-by | [agent:bob-cli-ji.7.1.4--5][1] | Need phase scope, notes, and current status after Test hang | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ji.7.1.4.md

<!-- sase:referenced-by:end -->
