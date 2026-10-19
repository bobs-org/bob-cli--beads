# Bead: bob-cli-9k.7 — Bob Mac Capture agenda shows homes

[Bead Pages](../README.md) / [bob-cli-9k](README.md) / bob-cli-9k.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.4t.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.4t.linker.w0.md) · **Assignee:** `bob-cli-9k.7` · **Size:** small
**Created:** 2026-10-18 16:35:50 EDT · **Closed:** 2026-10-18 18:12:14 EDT
**Plan:** [202610/pomodoro\_homes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/pomodoro_homes.md)

## Description

mac-agenda: decode the additive `homes` object. Unnamed agenda and Refs Today entries show the derived label instead of "Untitled Pomodoro", and named entries gain a muted chip with an area-hue dot. Add fixtures and tests, and gate on portable-check plus macOS CI.

## Notes

[2026-10-18T22:12:10Z · bob-cli-9k.7] PROPOSED FOLLOW-UP: Mac just typecheck-tests fails on untouched Tests/BobMacCaptureTests/RefsLibraryTests.swift — cannot find RefsNewestTests in scope (that helper lives in RefsCoreTests) and the compiler times out type-checking those XCTAssertTrue closures. Reproduced after our BobMacCapture* sources compiled cleanly; the file is unchanged in this phase. Confirm on origin/master and either share the helper or inline the ISO timestamps.

[2026-10-18T22:12:14Z · bob-cli-9k.7] Decoded additive homes on the idle agenda and Refs Today. Unnamed rows use homes.label (secondary style) instead of Untitled Pomodoro; named rows show a muted chip with an R8 hue dot. Fixtures cover named-suppressed, named-chip, unnamed-label, unlinked, and legacy. just portable-check passed (1376 tests). Scratch Mac typecheck compiled BobMacCapture/PomodoroHomes sources; typecheck-tests then failed on pre-existing RefsLibraryTests/RefsNewestTests (recorded as PROPOSED FOLLOW-UP). README Idle agenda documents homes. No leftover --epic-symbol entries.

## Dependencies

- **Depends on:** [bob-cli-9k.4](bob-cli-9k.4.md) ✓ · ⧖ 2026-10-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-9k.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9k.7/README.md) | [bob-cli-9k.7](bob-cli-9k.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@e5cd4e1`](https://github.com/bobs-org/bob-mac-capture/commit/e5cd4e1c3f3c12a4b83b86c409a378a67e0cd2c9) | feat(agenda): show derived Pomodoro homes on idle agenda and Refs Today | [bob-cli-9k.7](bob-cli-9k.7.md) | 2026-10-18 18:13:19 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-9k.7][1] | Need remaining notes, epic-symbols, and live-surfaces contract for mac-agenda | 2 |
| read-by | [agent:bob-cli-9k.8.land--1][2] | Need prior phase evidence and dispositions | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9k.7/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-9k.8.land.md

<!-- sase:referenced-by:end -->
