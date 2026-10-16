# Bead: bob-cli-8f.3 — Refs panel card, ⌘N routing, toast, and docs

[Bead Pages](../README.md) / [bob-cli-8f](README.md) / bob-cli-8f.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.7y](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.7y.md) · **Assignee:** `bob-cli-8f.3` · **Size:** medium
**Created:** 2026-10-16 10:04:17 EDT · **Closed:** 2026-10-16 12:58:25 EDT
**Plan:** [202610/refs\_link\_to\_today.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/refs_link_to_today.md)

## Description

mac_ui: wire ⌘N through RefsKeyRouter, RefsPanelModel, and RefsPanelController. Build the RefsTodayLinkCardView in the rename card's slot. Generalize the copy HUD into a reusable glass toast with a Today style and panel-anchored placement. Add an optimistic Today-pill overlay, refresh, VoiceOver announcements, and system notifications when the panel is hidden. Add the ⌘K action, footer hint, README sections, and model, router, and design tests.

## Notes

[2026-10-16T16:58:25Z · bob-cli-8f.3] Verified: portable-check passed on athena, with 1,276 tests and 0 failures; git diff --check passed; epic-symbol check reported no remaining entries. The final macOS bundle/UI typecheck remains unverified because the Mac became unreachable during the incremental rebuild after a missing RefsCore import was corrected.

[2026-10-16T17:17:08Z · bob-cli-8f.3--2] Verified: portable-check on athena executed 1,276 tests with 0 failures. Fresh macOS scratch copy: Scripts/bundle.sh built BobMacCapture (release, 80.94s) and just typecheck-tests passed BobMacCaptureTests, BobMacCaptureInstallHelperTests, CaptureCoreTests, and RefsCoreTests against the XCTest stub. git diff --check clean. epic-symbols has no remaining entries. Bead status left closed.

## Dependencies

- **Depends on:** [bob-cli-8f.2](bob-cli-8f.2.md) ✓ · ⧖ 2026-10-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-8f.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-8f.3.md) | [bob-cli-8f.3](bob-cli-8f.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@3a6db2b`](https://github.com/bobs-org/bob-mac-capture/commit/3a6db2bd120d51a212e5dc0cdf04486b60a2bec1) | feat(refs): wire Link to Today card, toast, and ⌘N routing | [bob-cli-8f.3](bob-cli-8f.3.md) | 2026-10-16 13:18:16 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-8f.3--2][1] | Need the phase scope, design file, notes, and current status after prior monitor failures | 1 |
| read-by | [agent:bob-cli-8f.land--2][2] | Need refreshed child status and prior follow-up outcomes before normal epic closure | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-8f.3.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-8f.land.md

<!-- sase:referenced-by:end -->
