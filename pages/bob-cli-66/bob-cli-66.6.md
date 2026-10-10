# Bead: bob-cli-66.6 — Transitions, countdown, stale and error states, accessibility, signposts, README

[Bead Pages](../README.md) / [bob-cli-66](README.md) / bob-cli-66.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.48.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.48.linker.w0.md) · **Assignee:** `bob-cli-66.6` · **Size:** medium
**Created:** 2026-10-09 17:42:23 EDT · **Closed:** 2026-10-09 21:30:22 EDT
**Plan:** [202610/idle\_capture\_pomodoro\_agenda.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/idle_capture_pomodoro_agenda.md)

## Description

mac-agenda-polish: add the first-keystroke dim-hold, the in-place cross-fade, the Now countdown, stale, loading, unsupported, and multiple-timed states, a Settings diagnostic, accessibility containers and values, `agenda-*` signposts, a show-path spawn guard test, and the README rewrite of the no-dead-space principle plus a new `## Idle agenda` section.

## Notes

[2026-10-10T01:30:22Z · bob-cli-66.6--1] CI green: https://github.com/bobs-org/bob-mac-capture/actions/runs/38012589878 SHA f8c9c28 (lint, build, Test incl. 887 CaptureCoreTests, bundle, smoke, install all success). Reviewed 10 render-fixture agenda PNGs covering all 7 states (current, nothing-running, heavy folded, empty, multiple-timed, current-stale, current-overdue) in light+dark at 620+760 widths: thin-material pane, quiet title row, Now pink rail+faint wash, reused number badges/status glyphs, chip capsules incl. Later name strip, stale clock.badge.exclamationmark + Couldn't refresh, orange overdue 8m — no misalignment, clipping, contrast, or truncation; no fix-forward needed. Checkout clean at f8c9c28; epic-symbols reports no leftovers.

## Dependencies

- **Depends on:** [bob-cli-66.5](bob-cli-66.5.md) ✓ · ⧖ 2026-10-09
- **Blocks:** [bob-cli-66.7](bob-cli-66.7.md) ✓ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-66.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-66.6.md) | [bob-cli-66.6](bob-cli-66.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@f8c9c28`](https://github.com/bobs-org/bob-mac-capture/commit/f8c9c28ce4a7ac1d4b08ba2a07dfde4df4ab9e27) | feat(agenda): transitions, countdown, states, accessibility, signposts, README | [bob-cli-66.6](bob-cli-66.6.md) | 2026-10-09 21:17:12 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-66.6][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-66.6.md

<!-- sase:referenced-by:end -->
