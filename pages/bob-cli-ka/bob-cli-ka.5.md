# Bead: bob-cli-ka.5 — Bob Mac Capture place menu, highlighting, and grouped preview

[Bead Pages](../README.md) / [bob-cli-ka](README.md) / bob-cli-ka.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1b9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1b9.md) · **Assignee:** `bob-cli-ka.5` · **Size:** large
**Created:** 2026-11-11 09:22:46 EST · **Closed:** 2026-11-11 18:04:21 EST
**Plan:** [202611/notebook\_section\_bullets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/notebook_section_bullets.md)

## Description

mac: in bob-mac-capture, generalize the drawer menu into one place menu painted from Bob's chrome, open it for section bullets and glued notebook sections, keep the empty-notebook hint, group the notebook batch preview by section, regenerate fixtures, update protocol docs, and watch macOS CI to green.

## Notes

[2026-11-11T19:36:18Z · bob-cli-ka.5] PROPOSED FOLLOW-UP: Empty glued notebook section completion omits place_menu — source inspection at bob-cli 1a9b68289f65f57d0b4a1bc3d9f955f82ae0291a shows engine.rs place_menu_for requires is_notebook_section_menu(candidates) for context section, but that predicate uses rows.iter().any and is false with zero rows even when notebook_menu_target resolved the notebook. Thus a bare @nb# on a notebook without H2s cannot deliver Type a section name; bullet context does carry the hint. This is source-backed evidence, not a runtime reproduction. Land agent should confirm with a scratch-vault CLI regression and use the resolved notebook target to retain chrome for empty glued responses; the Mac must not infer notebook identity or invent the missing chrome.

[2026-11-11T21:36:21Z · bob-cli-ka.5--3] PROPOSED FOLLOW-UP: Mac scratch `just typecheck-tests` still fails on clean-base @MainActor alias tests (`CaptureModifierAliasTests` / `CaptureRelationEqualsAliasTests` mutate `ledgerSuites` from nonisolated `tearDown`). Same four isolation errors as tracked bead bob-cli-jy; this place-menu tree did not add typecheck errors. `Scripts/bundle.sh` on a disposable `/tmp` copy compiled after replacing SwiftUI `.accessibilityHelp` with `.accessibilityHint` on the capture editor. Exact-SHA macOS CI Build/Test/Bundle remains the close gate.

[2026-11-11T22:07:32Z · dd--1] DISCOVERED ISSUE: macos-ci-check on the accessibilityHelp delete (run 43105632578) built, then failed three 4a69ed2 tests: testNotebookCreateSectionUsesDottedUnderlineAndExistingClearsIt, testNotebookNewSectionUsesDottedPurpleUnderlineAndRepaintClearsIt (dotted create underline not cleared on existing/generic repaint), and testAcceptingDrawerCandidateInsertsSlugAndLandsCaret (Tab on unselected drawer placeMenu is a no-op because acceptSelectedCompletion returns false when selectedCompletionIndex is nil). Exact-SHA master run 43100764208 never executed these tests. Hotfix not landed. Full evidence on epic bob-cli-ka. Not the empty glued place_menu PROPOSED FOLLOW-UP.

[2026-11-11T22:20:28Z · bob-cli-ka.5--4] Record Test-step failures and the three Swift fixes before restaging macOS CI Exact-SHA macOS CI run 43104852429 failed Test on snapshot c4ea007 (Build passed). Failures: CaptureAliasTipPanelTests.testEditBeforeTheReplyDropsTheTip (dropped[sigilEdited] nil because deferAliasTipOpportunity overwrote an existing dropReason); CaptureEditorHighlightTests.testNotebookCreateSectionUsesDottedUnderlineAndExistingClearsIt and CapturePanelModelTests.testNotebookNewSectionUsesDottedPurpleUnderlineAndRepaintClearsIt (AttributedString underlineStyle=nil left the dotted create underline); CapturePanelModelTests.testAcceptingDrawerCandidateInsertsSlugAndLandsCaret (placeMenu unselected-accept guard applied to drawers, so Tab no longer took the first row). Fixes: notebook_section-only unselected-accept no-op; empty NSUnderlineStyle to clear create underline; latch dropReason. Disposable Mac scratch Scripts/bundle.sh succeeded (Build complete, 127.86s) and was deleted. just portable-check passed (2499 tests, 0 failures). just typecheck-tests still fails only the known bob-cli-jy MainActor ledgerSuites tearDown errors. -r

[2026-11-11T23:04:21Z · bob-cli-ka.5--5] Exact-SHA macOS CI run 43111119712 passed the required macOS 26 SwiftPM steps for snapshot SHA ac6ddc5d45343440545c2ab02b78a37f3b5d727d (tree 8371823ceee041bb36654fbb7454dc41e06c6681): Lint Swift formatting, Build, Test, Bundle, Verify plist and signature, Launch smoke test, and Install and reinstall. URL: https://github.com/bobs-org/bob-mac-capture/actions/runs/43111119712

That snapshot is origin/master 6cbbddf6eb9192e8d20ed17cb0206fc257a91102 plus the Test-failure working-tree fixes: Tab on an unselected drawer still takes the first row (unselected-accept no-op is notebook_section only); existing-section repaint clears the dotted create underline with NSUnderlineStyle([]); deferAliasTipOpportunity latches the first dropReason so sigilEdited is kept.

Empty glued @nb# menus still paint only Bob's chrome. just typecheck-tests still fails only the known bob-cli-jy MainActor ledgerSuites tearDown errors in CaptureModifierAliasTests/CaptureRelationEqualsAliasTests; that is a recorded PROPOSED FOLLOW-UP, not a place-menu regression. No --epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-ka.2](bob-cli-ka.2.md) ✓ · ⧖ 2026-11-11
- **Depends on:** [bob-cli-ka.3](bob-cli-ka.3.md) ✓ · ⧖ 2026-11-11
- **Depends on:** [bob-cli-ka.4](bob-cli-ka.4.md) ✓ · ⧖ 2026-11-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ka.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ka.5.md) | [bob-cli-ka.5](bob-cli-ka.5.md) | 3 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@4a69ed2`](https://github.com/bobs-org/bob-mac-capture/commit/4a69ed25bec6a6398d64e1873eccb928d21af96a) | feat(capture): paint notebook section place menus from Bob chrome | [bob-cli-ka.5](bob-cli-ka.5.md) | 2026-11-11 16:10:15 EST |
| bob-mac-capture | [`bob-mac-capture@26e9f0a`](https://github.com/bobs-org/bob-mac-capture/commit/26e9f0a8661e0013e6baf73381c95dde29243548) | fix(capture): use accessibilityHint for notebook section editor help | [bob-cli-ka.5](bob-cli-ka.5.md) | 2026-11-11 16:38:09 EST |
| bob-mac-capture | [`bob-mac-capture@7fceb52`](https://github.com/bobs-org/bob-mac-capture/commit/7fceb525141f5facb2a7d7de94efbdf9362d6839) | fix(capture): keep drawer Tab accept and clear create-section underlines | [bob-cli-ka.5](bob-cli-ka.5.md) | 2026-11-11 18:05:43 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ka.5--2][1] | Need assigned-bead scope, notes, and remaining work before finishing notebook place-menu implementation | 2 |
| read-by | [agent:bob-cli-ka.5--3][1] | Need assigned bead scope after macOS CI Build failure | 1 |
| read-by | [agent:bob-cli-ka.5--5][1] | Need current bead status and close criteria before deciding whether exact-SHA macOS CI passed | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ka.5.md

<!-- sase:referenced-by:end -->
