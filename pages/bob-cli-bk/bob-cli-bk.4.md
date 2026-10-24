# Bead: bob-cli-bk.4 — Route card in the Bob Mac Capture panel

[Bead Pages](../README.md) / [bob-cli-bk](README.md) / bob-cli-bk.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.a9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.a9.md) · **Assignee:** `bob-cli-bk.4` · **Size:** medium
**Created:** 2026-10-24 14:00:27 EDT · **Closed:** 2026-10-24 18:09:21 EDT
**Plan:** [202610/capture\_inbox\_routing.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_inbox_routing.md)

## Description

mac-route-card: the panel shows the route card on Return after any pull-in card, resubmits the answers, handles refusals, documents the card, and lands the memory updates.

## Notes

[2026-10-24T21:39:21Z · bob-cli-bk.4] PROPOSED FOLLOW-UP: Add a decisions record for capture inbox routing once the epic land agent triages the skipped memory decision.

[2026-10-24T22:09:21Z · bob-cli-bk.4--3] Implemented the route card and authorized glossary/docs updates. Verified just portable-check on athena (1,642 tests passed), just docs-gen, just docs-check (all gates including 448 docs tests), sase memory init --no-commit, and git diff --check in root and sidecar; re-read glossary:inbox-file. Epic symbols: none. The earlier Mac scratch compile reported a route-card foreground-style error and a CapturePanelView type-check timeout; the linked source now uses explicit Color types and splits the body modifiers, but the Mac went offline before resync/retry or scratch cleanup. Local format-lint also could not run because Linux has no Apple developer tools. portable-check cannot type-check Sources/BobMacCapture or Tests/BobMacCapture, so current macOS format/build/test targets remain unverified.

## Dependencies

- **Depends on:** [bob-cli-bk.3](bob-cli-bk.3.md) ✓ · ⧖ 2026-10-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-bk.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-bk.4.md) | [bob-cli-bk.4](bob-cli-bk.4.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e70f9ea`](https://github.com/bobs-org/bob-cli/commit/e70f9ea40a7be87ffc761b851eda2613d288e9c8) | docs(memory): explain capture inbox routing | [bob-cli-bk.4](bob-cli-bk.4.md) | 2026-10-24 18:10:17 EDT |
| bob-mac-capture | [`bob-mac-capture@7bfa312`](https://github.com/bobs-org/bob-mac-capture/commit/7bfa31275b3dccbb72e15f664065bddd8363a39d) | feat(capture): add inbox route card | [bob-cli-bk.4](bob-cli-bk.4.md) | 2026-10-24 18:11:20 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-bk.4--3][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-bk.4.md

<!-- sase:referenced-by:end -->
