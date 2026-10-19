# Bead: bob-cli-9k.8.4 — Bob Mac Capture and chezmoi: no derived routing, hollow forecast dots, override labels

[Bead Pages](../README.md) / [bob-cli-9k.8](bob-cli-9k.8.md) / bob-cli-9k.8.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-9k.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-9k.land.md) · **Assignee:** `bob-cli-9k.8.4` · **Size:** medium
**Created:** 2026-10-18 20:20:12 EDT · **Closed:** 2026-10-18 21:41:15 EDT
**Plan:** [202610/pomodoro\_homes\_landing.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/pomodoro_homes_landing.md)

## Description

mac: stop Refs Today Link from selecting or routing by `homes.label`, name the derived label in its toast, draw forecast dots hollow, add the Later strip "for", fix the HACK fixture, show the derived label in the override banner from `override.previous.homes`, refresh fixtures from real bob output, compile on the Mac and check CI; in chezmoi add the unnamed-derived tmux status sample.

## Notes

[2026-10-19T01:41:15Z · bob-cli-9k.8.4] Mac: RefsTodayLinkCard no longer matches/selects on homes.label (R7), toast names derived label via destination row lookup; agenda chips draw ring for forecast / filled for attributed with homeIsForecast plumbed through rows; Later strip spoken text uses spoken names ('for <label>'); override.previous/demoted decode optional homes (Codable added to CaptureAgendaHomes family) with banner/restart/demoted rows showing derived label and falling back to session text; HACK fixtures fixed to 'bob · dev' to match parts, unnamed override fixture gains homes, legacy no-homes payloads kept. Verified: just portable-check green (1383 tests, 0 failures, format lint clean); chezmoi tmux_status_right 6/6 incl new unnamed-derived sample; hammerspoon busted 150/0. NOT verified: Mac typecheck-tests (mac offline, SSH timed out) and macOS CI (master CI red pre-existing; changes unpushed by phase worker). Fixtures hand-reconciled to the Homes/label contract, not regenerated from a live vault run.

## Dependencies

- **Depends on:** [bob-cli-9k.8.2](bob-cli-9k.8.2.md) ✓ · ⧖ 2026-10-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-9k.8.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9k.8.4/README.md) | [bob-cli-9k.8.4](bob-cli-9k.8.4.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@3a67176`](https://github.com/bobs-org/bob-mac-capture/commit/3a671761fe574eba68d290feb9f9b7af62207da1) | feat(capture): no derived routing in Refs Today Link, hollow forecast dots, override labels | [bob-cli-9k.8.4](bob-cli-9k.8.4.md) | 2026-10-18 21:42:38 EDT |
| chezmoi | [`chezmoi@d908496`](https://github.com/bbugyi200/dotfiles/commit/d90849608e4c4dc83286f08008cce541c4b119c2) | test(tmux): cover unnamed derived-label pomodoro status sample | [bob-cli-9k.8.4](bob-cli-9k.8.4.md) | 2026-10-18 21:43:37 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-9k.8.4][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-9k.8.land--1][2] | Need phase evidence and all notes before recording the remaining epic gate | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9k.8.4/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-9k.8.land.md

<!-- sase:referenced-by:end -->
