# Bead: bob-cli-iu.2 — Mac Capture escapes the \`.\` → \`@\` alias with a fast \`..\`

[Bead Pages](../README.md) / [bob-cli-iu](README.md) / bob-cli-iu.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.d0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.d0.md) · **Assignee:** `bob-cli-iu.2` · **Size:** medium
**Created:** 2026-11-08 16:46:40 EST · **Closed:** 2026-11-08 17:56:56 EST
**Plan:** [202611/dot\_route\_alias.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/dot_route_alias.md)

## Description

mac-dot-fast-escape: generalize the `=` gesture arm and probe by key so a fast `..` after Bob's `@` reply types one `.`, add Space/Escape restores, fake-bob tests, and docs.

## Notes

[2026-11-08T21:48:43Z · bob-cli-iu.2] --list

[2026-11-08T22:12:32Z · bob-cli-iu.2] PROPOSED FOLLOW-UP: docs-check fails identically on clean tree — bob-plugins mount collides with committed docs/reference/plugins/index.md (environmental, outside phase scope)

[2026-11-08T22:56:40Z · bob-cli-iu.2] PROPOSED FOLLOW-UP: macOS CI Test step red on identical separator tests in master run 42523594058 (base SHA 2a39c2ff) and phase run 42531359678 — 16 distinct CaptureSeparatorToggleTests failures reproduce on the clean tree, outside phase scope

[2026-11-08T22:56:56Z · bob-cli-iu.2] Implemented dot-route fast-escape. Verified: athena portable-check green (swift format lint clean, build ok, 2268 tests 0 failures); macOS CI run 42531359678 on fixed snapshot: Lint success, Build success, Test step red only on 16 pre-existing CaptureSeparatorToggleTests failures identical to clean-master run 42523594058 (all reproduced on base tree, recorded as follow-ups); new CaptureDotRouteAliasTests suite passed. Physical Mac offline so local typecheck-tests impossible; docs-check fails identically on clean tree (pre-existing mount collision, recorded as follow-up).

[2026-11-08T22:57:24Z · bob-cli-iu.2] PROPOSED FOLLOW-UP: closest open tracker is bob-cli-h7 (macOS CI red, backslash/chip/error-prefix set); closed bob-cli-f3 previously covered + separator-toggle tests. The 16 failing tests here need triage against those sets before any +1.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-iu.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-iu.2.md) | [bob-cli-iu.2](bob-cli-iu.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@e7ddfc6`](https://github.com/bobs-org/bob-mac-capture/commit/e7ddfc66a7c150fbca899be44ed0474fcc06769e) | feat(mac-capture): escape dot-route alias with fast .. and restores | [bob-cli-iu.2](bob-cli-iu.2.md) | 2026-11-08 18:03:13 EST |
