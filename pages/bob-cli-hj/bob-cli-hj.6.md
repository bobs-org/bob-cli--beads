# Bead: bob-cli-hj.6 — Bob Mac Capture segment typing, picker, card, and guard

[Bead Pages](../README.md) / [bob-cli-hj](README.md) / bob-cli-hj.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.18s](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.18s.md) · **Assignee:** `bob-cli-hj.6` · **Size:** medium
**Created:** 2026-11-05 14:25:25 EST · **Closed:** 2026-11-06 05:42:38 EST
**Plan:** [202611/past\_pomodoro\_segment\_suffix.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/past_pomodoro_segment_suffix.md)

## Description

mac: add - to the rewrite trigger keys, style the segment span, render picker rows, decode and show the segment line and cut note on the past card, and send --expect-past-windows with a re-preview on refusal; regenerate fixtures and update protocol docs.

## Notes

[2026-11-06T10:42:04Z · bob-cli-hj.6--r] PROPOSED FOLLOW-UP: Add Bob-reported theme hue to past-segment candidates — the segment completion wire omits the Pomodoro hue, so Mac picker rows can only use a generic tint.

[2026-11-06T10:42:08Z · bob-cli-hj.6--r] PROPOSED FOLLOW-UP: Resolve mounted Bob docs-check drift — Mac lint, generated-content, build, URL, lychee, tutorial, and media checks pass, but docs unit tests fail a mounted Bob CLI contract snapshot; earlier glossary drift and the task-merge link are tracked by bob-cli-hl.6 and bob-cli-hs.

[2026-11-06T10:42:12Z · bob-cli-hj.6--r] PROPOSED FOLLOW-UP: Triage current-base macOS test failures — run 42201738623 has the editor word-motion, MoveChoice, comma-route, and separator-alias/backslash failures tracked by bob-cli-h7; testFooterContractPinsHintsAndAccessibilityText also fails on base 6f4e279 because closeSupported=false omits Ctrl-X and Ctrl-Shift-X while the assertion expects them. All segment-specific tests pass.

[2026-11-06T10:42:38Z · bob-cli-hj.6--r] Verified Bob Mac Capture segment picker/card and stale-window behavior; portable suite passed and exact-SHA macOS CI run 42201738623 passed all segment tests (fast Return, second dash, segment undo, ungated dash, and links-to rewrite). Remaining CI failures are documented baseline/current-base cases; docs drift and missing hue follow-ups recorded. Epic symbols: none.

## Dependencies

- **Depends on:** [bob-cli-hj.4](bob-cli-hj.4.md) ✓ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-hj.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hj.6.md) | [bob-cli-hj.6](bob-cli-hj.6.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@16c79f6`](https://github.com/bobs-org/bob-mac-capture/commit/16c79f6901b3cc070934ac8486adac3d00861f4a) | feat(capture): add past Pomodoro segment UI support | [bob-cli-hj.6](bob-cli-hj.6.md) | 2026-11-05 22:20:00 EST |
| bob-mac-capture | [`bob-mac-capture@9578c66`](https://github.com/bobs-org/bob-mac-capture/commit/9578c6634f345dd7d4d7563a8e0980d10b9c6fe0) | fix(capture): preserve past-segment submit after rewrite | [bob-cli-hj.6](bob-cli-hj.6.md) | 2026-11-06 06:18:40 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hj.6--9][1] | Need the current phase scope, design file, notes, and close requirements | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hj.6.md

<!-- sase:referenced-by:end -->
