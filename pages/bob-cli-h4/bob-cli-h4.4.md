# Bead: bob-cli-h4.4 — Mac transfer card, status line, offers, notifications, and VoiceOver

[Bead Pages](../README.md) / [bob-cli-h4](README.md) / bob-cli-h4.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.188](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.188.md) · **Assignee:** `bob-cli-h4.4` · **Size:** medium
**Created:** 2026-11-04 14:57:19 EST · **Closed:** 2026-11-05 06:50:30 EST
**Plan:** [202611/transfer\_previews.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/transfer_previews.md)

## Description

mac-transfer-card: replace the monospace transfer bands and the wire-word standard header with one designed transfer card that mirrors the draft. The card shows the verb, the source rows, an `↓ into` connector, the destination, consequence rows, the TODAY badge, and the offer rows. Also rewrite the status line, notification copy, and VoiceOver summary, regenerate rich recorded fixtures, and add design renders and docs.

## Notes

[2026-11-04T23:58:40Z · bob-cli-h4.4--5] Mac verification remains pending. The 45-minute retry failed before compilation because the remote shell received the literal $scratch path and could not cd into it. Tailscale currently reports the Mac offline, last seen 17 minutes ago; the rsynced scratch copy could not be checked or removed while offline. Earlier just portable-check (2,123 tests, 0 failures, 1 skipped), just docs-check, and 10 focused transfer presentation tests passed. Do not close until the Mac scratch bundle and just typecheck-tests are verified.

[2026-11-05T11:37:32Z · bob-cli-h4.4] PROPOSED FOLLOW-UP: Existing macOS CI failures remain outside transfer scope — exact phase commit e9dc5bd run 41943309819 and its clean parent edb2f48 run 41937019961 have the identical set of 14 assertion errors (9 tests) in CaptureBackslashGotoTests, CaptureEditorWordMotionTests, and CaptureSeparatorToggleTests; comparison found zero added or removed assertion errors. Related tracking: bob-cli-h7 and bob-cli-h8.5 note #2. Transfer presentation, card design renders, status/footer, and both transfer notification tests all passed in phase CI. https://github.com/bobs-org/bob-mac-capture/actions/runs/41943309819 https://github.com/bobs-org/bob-mac-capture/actions/runs/41937019961

[2026-11-05T11:39:08Z · bob-cli-h4.4] Verification resumed: implementation is already landed as bob-mac-capture e9dc5bd (current clean linked checkout c95094d). CI 41943309819 compiled macOS Build and passed CaptureTransferPresentationTests, CaptureTransferCardDesignTests (24 images: six fixtures x 620/760 x light/dark), transfer status/footer test, and both transfer notification tests. Reviewed one render of each of the six scenarios; source/destination order, chips, consequences, embedded offer/TODAY row, new containers, and muted unchanged state render correctly. Earlier portable-check and docs-check remain passing evidence from note #1; no source changes in this turn. epic-symbols reports none. Mac SSH is now online; remaining work is the scratch release bundle and just typecheck-tests, with corrected literal-path quoting and guaranteed cleanup on ordinary success/failure. A monitored verification will hand its result to a successor to close only bob-cli-h4.4.

[2026-11-05T11:50:30Z · bob-cli-h4.4--1] Verified implementation already landed in bob-mac-capture e9dc5bd. Final monitor pcg0rend0xxf (tool run 0f50a830cb5932e03436fdb154da0585) completed 2026-11-05 with exit 0: fresh Mac scratch release bundle via Scripts/bundle.sh passed, just typecheck-tests passed BobMacCaptureTests, BobMacCaptureInstallHelperTests, CaptureCoreTests, and RefsCoreTests, and scratch cleanup was verified. This completes the remaining verification from note #1. Prior evidence retained: portable-check 2,123 tests with 0 failures and 1 skipped; docs-check passed; phase CI 41943309819 passed transfer presentation, card design renders, status/footer, and both notification tests; all six transfer design scenarios reviewed. Full CI has only the identical 14 assertion errors from clean parent run 41937019961, recorded in PROPOSED FOLLOW-UP note #2 citing bob-cli-h7 and bob-cli-h8.5. Re-ran sase bead epic-symbols bob-cli-h4.4: no entries. No source edits were needed. Closing only bob-cli-h4.4.

## Dependencies

- **Depends on:** [bob-cli-h4.2](bob-cli-h4.2.md) ✓ · ⧖ 2026-11-04
- **Blocks:** [bob-cli-h4.5](bob-cli-h4.5.md) ✓ · ⧖ 2026-11-04

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-h4.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-h4.4.md) | [bob-cli-h4.4](bob-cli-h4.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@e9dc5bd`](https://github.com/bobs-org/bob-mac-capture/commit/e9dc5bd91253cf0ad09671eb8c724cb5a37453a5) | feat(capture): render transfer previews as cards | [bob-cli-h4.4](bob-cli-h4.4.md) | 2026-11-04 19:42:16 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-h4.4--5][1] | Record the final verification state before ending this turn | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-h4.4.md

<!-- sase:referenced-by:end -->
