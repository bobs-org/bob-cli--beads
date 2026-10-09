# Bead: bob-cli-5w.5 — Successor Links in Bob Mac Capture previews and notifications

[Bead Pages](../README.md) / [bob-cli-5w](README.md) / bob-cli-5w.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.0p.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.0p.linker.w0.md) · **Assignee:** `bob-cli-5w.5` · **Size:** medium
**Created:** 2026-10-09 11:54:15 EDT · **Closed:** 2026-10-09 14:52:52 EDT
**Plan:** [202610/successor\_links.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/successor_links.md)

## Description

mac: in bob-mac-capture, decode the additive successor JSON defensively. Render successors in the `!` and close previews: destination capsule, minted-ID caption, reasons, and muted still-blocked rows. Badge unblocked lines in block diffs, add one notification line, and fix Open Note(s). Ships real-bob fixtures, tests, a README update, and green macOS CI.

## Notes

[2026-10-09T18:47:17Z · bob-cli-5w.5] PROPOSED FOLLOW-UP: Record "a closed planned task hands its slot to its successors" as a decisions strand (epic plan asked; auto-decision was no)

[2026-10-09T18:47:23Z · bob-cli-5w.5] PROPOSED FOLLOW-UP: Add a "Successor Link" glossary term (epic plan asked; auto-decision was no)

[2026-10-09T18:52:39Z · bob-cli-5w.5--1] PROPOSED FOLLOW-UP: Fix pre-existing macOS-only failure testKeyDrivenAssistParseServesCommaEdit (CaptureCloseTaskCommaTests.swift:403/415, condition timeout + nil vs 2) — fails identically on base 8c10d52 run 37973573511 and on f4a36e3 run 37975602555; unrelated to successor-links change

[2026-10-09T18:52:52Z · bob-cli-5w.5--1] Successor-links change f4a36e3 landed with all successor suites green on macOS CI (CaptureSuccessorPresentationTests, PomodoroCloseDesignTests render, NotificationServiceTests notice-line, TaskComplete fixture tests); 1673/1675 pass. Sole failure testKeyDrivenAssistParseServesCommaEdit reproduces identically on clean base 8c10d52 (run 37973573511), recorded as PROPOSED FOLLOW-UP; epic-symbols clean.

## Dependencies

- **Blocks:** [bob-cli-5w.11](bob-cli-5w.11.md) ✓ · ⧖ 2026-10-09
- **Depends on:** [bob-cli-5w.4](bob-cli-5w.4.md) ✓ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-5w.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-5w.5.md) | [bob-cli-5w.5](bob-cli-5w.5.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-5w.5][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-5w.5.md

<!-- sase:referenced-by:end -->
