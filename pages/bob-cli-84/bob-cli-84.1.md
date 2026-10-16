# Bead: bob-cli-84.1 — Stable signing identity and Accessibility status

[Bead Pages](../README.md) / [bob-cli-84](README.md) / bob-cli-84.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.7w](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.7w.md) · **Assignee:** `bob-cli-84.1` · **Size:** small
**Created:** 2026-10-15 17:50:48 EDT · **Closed:** 2026-10-15 18:04:58 EDT
**Plan:** [202610/highlights\_tabs\_switcher.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/highlights_tabs_switcher.md)

## Description

signing: `just install` signs with a stable self-signed "Bob Mac Capture Local" identity when it exists, and otherwise falls back to ad-hoc with a loud warning. `bundle.sh` keeps its ad-hoc default for agent scratch builds. The ad-hoc warning now mentions Accessibility. Settings › References shows "Highlights tabs: Allowed / Not allowed" through a small AccessibilityTrust helper. The README documents creating the identity.

## Notes

[2026-10-15T22:04:40Z · bob-cli-84.1] PROPOSED FOLLOW-UP: Add decisions record stating Bob Mac Capture uses Accessibility only to read and select Highlights tabs (epic plan decision_record=false; skipped per phase DECISIONS)

[2026-10-15T22:04:45Z · bob-cli-84.1] PROPOSED FOLLOW-UP: just typecheck-tests fails identically on clean base (unable to load standard library for arm64-apple-macosx26.0 under CLT); BobMacCaptureTests green only in CI

[2026-10-15T22:04:58Z · bob-cli-84.1] signing phase done in bob-mac-capture@2286ae3: install.sh resolves Bob Mac Capture Local w/ ad-hoc fallback warning + --print-resolved-identity (verified read-only on mac, prints -); bundle.sh unchanged; justfile install default empty; inspector ad-hoc text mentions Accessibility; AccessibilityTrust helper + Settings Highlights tabs row; README Signing docs. Verified: bash -n, resolver branches incl. fake-keychain, athena portable-check 1209 tests 0 failures, mac bundle.sh ad-hoc build+sign OK. typecheck-tests fails identically on base (env issue, filed follow-up).

## Dependencies

- **Blocks:** [bob-cli-84.3](bob-cli-84.3.md) ✓ · ⧖ 2026-10-15
- **Blocks:** [bob-cli-84.6](bob-cli-84.6.md) ✓ · ⧖ 2026-10-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-84.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-84.1/README.md) | [bob-cli-84.1](bob-cli-84.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@1cd958e`](https://github.com/bobs-org/bob-mac-capture/commit/1cd958e4c96a1f75f6b14f29f72b3c4833a6c22e) | feat(signing): sign with stable self-signed identity with ad-hoc fallback | [bob-cli-84.1](bob-cli-84.1.md) | 2026-10-15 18:06:11 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-84.1][1] | need full | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-84.1/README.md

<!-- sase:referenced-by:end -->
