# Bead: bob-cli-bc.12 — Menu-bar theme swatch

[Bead Pages](../README.md) / [bob-cli-bc](README.md) / bob-cli-bc.12

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2c.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2c.linker.w1.md) · **Assignee:** `bob-cli-bc.12` · **Size:** small
**Created:** 2026-10-24 07:52:22 EDT · **Closed:** 2026-10-24 08:57:32 EDT
**Plan:** [202610/pomodoro\_themes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/pomodoro_themes.md)

## Description

menubar: show the running session's theme swatch before the mac pom title in the chezmoi Hammerspoon indicator.

## Notes

[2026-10-24T12:57:19Z · bob-cli-bc.12] Verified: chezmoi Hammerspoon prepends catalog hue swatches before the mac pom title.

Automated: busted ./tests/hammerspoon — 192 successes (countdown split/hue/swatch policy; init fetch of `bob themes list -a -f json` on the existing re-sync command, light/dark hex, composite/exempt/unknown/failed fallbacks, name stays labelColor).

Mac (reachable 2026-10-24): live `bob` does not yet have `themes` (`unrecognized subcommand`); current session is overdue GTD. The new script still exits 0 on pomodoro success (`bob themes list … || true`), so a missing command leaves the title unchanged. Visual check needs a Mac `bob` that has `themes` plus chezmoi apply / Hammerspoon reload.

Manual check after apply:
1. `chezmoi apply ~/.hammerspoon` then Hammerspoon Reload Config (or full apply so the restart hook runs).
2. Confirm `bob themes list -a -f json` works on the Mac.
3. Running named non-exempt theme (e.g. BOB): colored ■ before the name; name/duration/tomato stay ordinary foreground; overdue red only on the status.
4. Composite (BOB + DECKS): two squares; GTD or unknown name: no square; idle worked total: no square.
5. Refresh / vault edit still re-syncs; failed `bob themes` keeps the pomodoro title.

[2026-10-24T12:57:32Z · bob-cli-bc.12] Chezmoi mac pom prepends catalog ■ swatches from bob themes list -a -f json on existing re-syncs; title text stays untinted; exempt/unknown/failed themes leave the title unchanged. busted tests/hammerspoon 192 ok. Mac live bob lacks themes yet so visual check is after apply (steps in the phase note).

## Dependencies

- **Blocks:** [bob-cli-bc.13](bob-cli-bc.13.md) ◐ · ⧖ 2026-10-24
- **Depends on:** [bob-cli-bc.2](bob-cli-bc.2.md) ✓ · ⧖ 2026-10-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-bc.12](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bc.12/README.md) | [bob-cli-bc.12](bob-cli-bc.12.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-bc.12][1] | Need full bead details including notes | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bc.12/README.md

<!-- sase:referenced-by:end -->
