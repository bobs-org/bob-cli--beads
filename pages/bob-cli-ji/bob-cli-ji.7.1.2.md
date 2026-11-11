# Bead: bob-cli-ji.7.1.2 — Event-note session, request ordering, and mutation undo

[Bead Pages](../README.md) / [bob-cli-ji.7.1](bob-cli-ji.7.1.md) / bob-cli-ji.7.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ji.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ji.7.md) · **Assignee:** `bob-cli-ji.7.1.2` · **Size:** medium
**Created:** 2026-11-10 10:29:45 EST · **Closed:** 2026-11-10 12:28:09 EST
**Plan:** [202611/mac\_event\_note\_mode.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_event_note_mode.md)

## Description

session: implement a dedicated event-note model with list/filter/select, explicit scope, separate per-scope drafts, debounced preview, serialized save/clear/undo, capability state, and stale-response rejection. Test its complete lifecycle with bounded fake-bob operations before panel wiring. Read the Session section.

## Notes

[2026-11-10T17:27:53Z · bob-cli-ji.7.1.2--1] PROPOSED FOLLOW-UP: Pre-existing CaptureAliasTipPanelTests waitUntil timeouts (testFilteringKeepsTheShownTipAnchoredToTheSigil, testOptionTypedHashOpensTheHashTip, testTypingQueryBeforeTheRouteListOpensKeepsTheTip) failed on exact-SHA run 42858829201 identically to base 8273c8f/aafed83 as recorded on bob-cli-ji.7.1.3; same class as flake bead bob-cli-jk — GcalNoteSessionTests all passed

[2026-11-10T17:28:09Z · bob-cli-ji.7.1.2--1] GcalNoteSession lifecycle with list/filter/select, per-scope drafts, 150ms preview, serialized save/clear/undo, stale-response rejection; athena portable-check 2438 tests 0 failures; exact-SHA macOS CI run 42858829201 GcalNoteSessionTests all passed; remaining CaptureAliasTipPanelTests waitUntil timeouts are pre-existing on base 8273c8f/aafed83 (bob-cli-jk / bob-cli-ji.7.1.3 follow-up)

## Dependencies

- **Depends on:** [bob-cli-ji.7.1.1](bob-cli-ji.7.1.1.md) ✓ · ⧖ 2026-11-10
- **Blocks:** [bob-cli-ji.7.1.4](bob-cli-ji.7.1.4.md) ✓ · ⧖ 2026-11-10

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ji.7.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ji.7.1.2.md) | [bob-cli-ji.7.1.2](bob-cli-ji.7.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@809b66a`](https://github.com/bobs-org/bob-mac-capture/commit/809b66abeaee819e72e1d89e78c2136dc7999db3) | feat(capture): add GcalNoteSession lifecycle | [bob-cli-ji.7.1.2](bob-cli-ji.7.1.2.md) | 2026-11-10 11:50:34 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ji.7.1.4--6][1] | Read the prior PROPOSED FOLLOW-UP for the same alias-tip timeouts | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ji.7.1.4.md

<!-- sase:referenced-by:end -->
