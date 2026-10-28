# Bead: bob-cli-dk.4 — Bob Mac Capture configured-theme rendering and warnings

[Bead Pages](../README.md) / [bob-cli-dk](README.md) / bob-cli-dk.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.151](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.151.md) · **Assignee:** `bob-cli-dk.4` · **Size:** medium
**Created:** 2026-10-28 07:47:10 EDT · **Closed:** 2026-10-28 10:32:33 EDT
**Plan:** [202610/configured\_pomodoro\_themes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/configured_pomodoro_themes.md)

## Description

mac: render `configured: false` themes with the dashed treatment, badge unconfigured create rows, show `theme_not_configured` in every preview and in Name-it without flicker, and scope Name-it chips to configured themes.

## Notes

[2026-10-28T14:32:33Z · bob-cli-dk.4] Mac Capture renders configured=false as dashed systemOrange 70% outline over muted fill, badges create rows with Not in your themes, shows theme_not_configured as one orange caption in every settled preview (caret-at-end prefix of a visible configured name is suppressed so BUILD never flickers; SNACK warns immediately), and Name-it chips come from visible configured_themes in config order with command warnings in the prompt. uniquingKeysWith first-wins on duplicate theme keys. Linux just portable-check: 1720 tests, 0 failures (cannot type-check BobMacCapture*). just docs-check passed. Mac scratch rsync to /tmp/bob-mac-capture-dk4 then just typecheck-tests: PASS BobMacCaptureTests, BobMacCaptureInstallHelperTests, CaptureCoreTests, RefsCoreTests (underlineStyle/underlineColor are Foundation NSUnderlineStyle + NSColor). Scratch deleted. Memory notes not edited in this phase.

## Dependencies

- **Depends on:** [bob-cli-dk.1](bob-cli-dk.1.md) ✓ · ⧖ 2026-10-28
- **Depends on:** [bob-cli-dk.2](bob-cli-dk.2.md) ✓ · ⧖ 2026-10-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-dk.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-dk.4/README.md) | [bob-cli-dk.4](bob-cli-dk.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@2497c41`](https://github.com/bobs-org/bob-mac-capture/commit/2497c412f20060bb90ec324daf8e41badcc44819) | feat(themes): render unconfigured Pomodoro themes with dashed treatment | [bob-cli-dk.4](bob-cli-dk.4.md) | 2026-10-28 10:33:48 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-dk.4][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-dk.4/README.md

<!-- sase:referenced-by:end -->
