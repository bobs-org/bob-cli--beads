# Bead: bob-cli-on.15.1.4 — Render requirement branches and wire their keyboard actions

[Bead Pages](../README.md) / [bob-cli-on.15.1](bob-cli-on.15.1.md) / bob-cli-on.15.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-on.15](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.15.md) · **Assignee:** `bob-cli-on.15.1.4` · **Size:** medium
**Created:** 2026-11-22 14:56:48 EST · **Closed:** 2026-11-22 19:25:01 EST
**Plan:** [202611/mac\_requirement\_close\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_requirement_close_card.md)

## Description

card_ui: render requirement sections first with bob-authored copy, depth glyphs, branch folds, consequences, scope summaries and accessible states. Wire Ctrl+X, Ctrl+Shift+X, Ctrl+Shift+T, Space/Tab and Ctrl+J through the existing router, controller and reason/recall UI. Preserve ordinary offer behavior, text focus, mark-all exclusions and Esc semantics; follow the card_ui section.

## Notes

[2026-11-22T23:20:55Z · bob-cli-on.15.1.4] card_ui implementation landed for review: requirement sections with Bob copy/scope/history, depth glyphs, folds, consequences, summary and accessible states; Ctrl+X Met, Ctrl+Shift+X Drop, Ctrl+Shift+T Carry, Space Carry-plus-pull, Tab advance, Ctrl+J pin through router/controller/reason-recall UI. Portable: just portable-check green (2699 tests, 0 failures). Scratch Mac: bundle.sh exit 0, just typecheck-tests PASS all 4 targets. macOS CI staged as p2rf1k via Scripts/macos-ci-check; exact-SHA verdict pending.

[2026-11-23T00:24:53Z · bob-cli-on.15.1.4--2] card_ui verification card_ui verification complete on fixed tree (HEAD 91db947c). Portable: just portable-check exit 0 on athena (Swift 6.0.3 Linux) — swift-format lint clean, swift build --build-tests + swift test: 2699 tests, 1 skipped, 0 failures. Scratch Mac (best-effort, mac online): rsync scratch copy excluding .git/.build to /tmp/bob-card-ui-scratch, ./Scripts/bundle.sh --identity - exit 0, just typecheck-tests exit 0 — PASS BobMacCaptureTests, BobMacCaptureInstallHelperTests, CaptureCoreTests, RefsCoreTests (4/4); scratch removed, Bryan checkout untouched. macOS CI exact-SHA green: Scripts/macos-ci-check exit 0 (monitor kx5dzsp1dpxh, 22m8s), run https://github.com/bobs-org/bob-mac-capture/actions/runs/45085290078, base 91db947c8e67c815ab842ff37424255716c2573b, snapshot 6c719fc58492b1a12334e2ca5b402ce3ee80027d (same tree, clean checkout); macOS 26 SwiftPM steps all ok: Lint/Build/Test/Bundle/Verify-plist/Launch-smoke/Install. Prior red run 45083102513 (snapshot fea13a70) failed only CapturePullInRequirementCardTests.testRequirementSectionsLeadWithBobCopyAndCounts (wrong expectation 1 req vs Bob Docs default 1 reqs); fixed by 91db947c asserting sections[0]=1 reqs and sections[1]=1 req — test bug, not a clean-base product failure. Fixture provenance: no fixture files changed in bab5e5cc..91db947c (14 .swift files only, Sources/Tests). Doc gates: no docs/ changed in this phase, just docs-check N/A; docs updates owned by integration bob-cli-on.15.1.5. epic-symbols: none. -r

[2026-11-23T00:25:01Z · bob-cli-on.15.1.4--2] card_ui done and verified: portable-check 2699 tests 0 failures; scratch Mac bundle.sh exit 0 and typecheck-tests 4/4 PASS; exact-SHA macOS CI green (run 45085290078, base 91db947c, snapshot 6c719fc5); test-expectation fix only, no fixture/doc changes, epic-symbols none.

## Dependencies

- **Depends on:** [bob-cli-on.15.1.3](bob-cli-on.15.1.3.md) ✓ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-on.15.1.5](bob-cli-on.15.1.5.md) ◐ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.15.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.15.1.4.md) | [bob-cli-on.15.1.4](bob-cli-on.15.1.4.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@7006f3e`](https://github.com/bobs-org/bob-mac-capture/commit/7006f3e7f8a3f3b4ec266029b3934bac62605551) | feat(capture): render requirement branches and wire their keyboard actions | [bob-cli-on.15.1.4](bob-cli-on.15.1.4.md) | 2026-11-22 18:23:32 EST |
| bob-mac-capture | [`bob-mac-capture@91db947`](https://github.com/bobs-org/bob-mac-capture/commit/91db947c8e67c815ab842ff37424255716c2573b) | fix(capture): correct requirement scope expectation to Bob order | [bob-cli-on.15.1.4](bob-cli-on.15.1.4.md) | 2026-11-22 18:47:52 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-on.15.1.4--1][1] | Need phase scope and design file to fix CI failure | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.15.1.4.md

<!-- sase:referenced-by:end -->
