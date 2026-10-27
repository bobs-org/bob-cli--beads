# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.4 — Refuse dirty ref-scan targets per PDF instead of failing the whole scan

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.4` · **Size:** large
**Created:** 2026-10-27 06:23:58 EDT · **Closed:** 2026-10-27 09:39:36 EDT
**Plan:** [202610/backlog\_batch17\_macos\_gate\_source\_backfill\_hook\_dedupe\_dirty\_scans\_swift\_format.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch17_macos_gate_source_backfill_hook_dedupe_dirty_scans_swift_format.md)

## Description

per-pdf-dirty-refusal: resolve bob-cli-b1 per the dirty_pdf decision so one autosaved Highlights PDF no longer refuses every other PDF in the scan.

## Notes

[2026-10-27T13:39:20Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.4--f] Implemented per-PDF dirty_targets holds: dirty plans skip all owned writes, clean plans continue, scan receipts and schema 1 remain intact, and Bob Mac Capture reports dirty holds with retry wording. Verification passed: Rust focused guard tests monitor wmmhdrhcwsd8 / ToolRun c80ce8bcb7fd88d3bb281a49fd25f0d9; bob-cli docs-check monitor zacdgq5f3wc8 / ToolRun b52aa97331861d5aff528d0835e7e98b; bob-cli just check monitor xx48rsw745nb / ToolRun 674766c8f58e85d01dcd1e7a379725bd; Mac portable-check monitor 6pxnhd7kecb3 / ToolRun 30911ed15414177300360e1ff9771008; Mac docs-check monitor 0hahmvcnvgch / ToolRun 9897406a76bf177638f640fd68d5dc1c. Earlier CLI fixture compile/format issues and Swift multiline-string formatting were corrected before these final passes. macOS CI passed: run 40509843189, snapshot fb90c52a3ee301a8cdbf4e25a45e68129186f834, branch ci/precommit/9afeb84481a33cceb67527ad1691d134, https://github.com/bobs-org/bob-mac-capture/actions/runs/40509843189. Every macOS 26 SwiftPM step passed except the two expected diagnostic-upload steps skipped: Set up job, Check out repository, Check scripts, Show toolchain, Lint Swift formatting, Build, Test, Upload render fixtures, Bundle, Verify plist and signature, Launch smoke test, Install and reinstall, Post Check out repository, Complete job. No failed tests. Scratch PRs #10-13 are closed and their branches were deleted. #10 stopped after the helper formatter raised KeyError on number; #11-13 produced no pull_request run within 300 seconds. The exact-SHA macos-ci-check push above supplied the required verdict. Leave bob-cli-b1 and every ancestor open.

[2026-10-27T13:39:36Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.4--f] Implementation and verification are recorded on this phase; all required local checks and exact-SHA macOS CI passed. bob-cli-b1 and all ancestors remain open.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.4.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.4](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.4.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`af3a8fd`](https://github.com/bobs-org/bob-cli/commit/af3a8fd4b5594d56a78d39312f2e36158be4d108) | feat(highlights-ref)!: report dirty scan targets as per-PDF holds | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.4](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.4.md) | 2026-10-27 09:40:32 EDT |
| bob-mac-capture | [`bob-mac-capture@f8a258f`](https://github.com/bobs-org/bob-mac-capture/commit/f8a258f411f48471026bffc859ac7b78c5c206db) | feat(refs): surface per-PDF dirty scan holds | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.4](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.4.md) | 2026-10-27 09:42:29 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.4--f][1] | Reconfirm the assigned dirty-scan phase in the workspace SDD bead store before closing | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.4.md

<!-- sase:referenced-by:end -->
