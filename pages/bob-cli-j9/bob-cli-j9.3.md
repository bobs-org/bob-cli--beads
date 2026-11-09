# Bead: bob-cli-j9.3 — Trigger, tip lane, and the completion-list host

[Bead Pages](../README.md) / [bob-cli-j9](README.md) / bob-cli-j9.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.3y.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.3y.linker.w0.md) · **Assignee:** `bob-cli-j9.3` · **Size:** medium
**Created:** 2026-11-09 12:18:38 EST · **Closed:** 2026-11-09 15:18:54 EST
**Plan:** [202611/capture\_alias\_typing\_tips.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_alias_typing_tips.md)

## Description

mac-completion-tips: record physically Shift- or Option-typed @ and # sigils, run the non-blocking alias-tip lane, admit tips only in the list's first frame, count adoption and escapes, add the Settings toggle and reset, pin the shared tip row in CompletionList, and add the Typing tips docs page.

## Notes

[2026-11-09T19:04:52Z · bob-cli-j9.3] PROPOSED FOLLOW-UP: macOS typecheck/Build fails on clean HEAD a5152aa with missing CaptureRelatedAction.addTo cases in CapturePanelModel.completeSimilarTaskIDAssignment and CapturePanelView similar-task insert-text switches — same ir.12 gap j6.land already pointed at bob-cli-ir; this phase did not touch those switches. Scratch typecheck compiled CaptureAliasTipRow/CaptureKeycap; portable-check 2390 tests passed.

[2026-11-09T19:06:38Z · bob-cli-j9.3] Added CaptureRelatedAction.addTo to the three exhaustive switches that blocked macOS Build on HEAD a5152aa (completeSimilarTaskIDAssignment and two similar-task insert-text switches), grouped with open/discard/unknown so this phase tests can run. Proper addTo ID-prompt copy still belongs to bob-cli-ir.

[2026-11-09T20:18:54Z · bob-cli-j9.3--2] Completion-list typing tips landed in bob-mac-capture 3131414 (feat) and 0eeba70 (CI-test fixes). Shift- or Option-typed at-sign and hash sigils start a 500ms latest-wins alias-tip lane; bob-proved Next time rows pin at the CompletionList first-frame foot. Hits and escapes still update the ledger with tips off. Settings has Typing Tips toggle and reset. Shared CaptureKeycap/CaptureAliasTipRow and docs/typing-tips.md are in place.

Verified:
- Athena just portable-check: 2390 tests, 0 failures
- just docs-check: only the five known over-cap pages; no new failures
- Scratch Mac typecheck compiled CaptureAliasTipRow/CaptureKeycap (prior turn); Build had been blocked by the ir.12 CaptureRelatedAction.addTo exhaustive-switch gap on HEAD a5152aa, which this phase grouped with open/discard/unknown so tests could run
- First exact-SHA macOS CI run 42680410174 (snapshot 2d1c316) failed Test: testFastSpaceRestoresEqualsBeforeTheCompletionReplyOpens (j9.1 restorable required picker source nil before Links To opened) and testRecordCardAccessibilityIdentitiesMatchPersistentState (companions VoiceOver now includes fixture default kelly)
- Fixes in 0eeba70: restore Space-to-equals in the pre-picker race window; expect "Companions, kelly, optional, default"
- Retry exact-SHA macOS CI run 42686364786 snapshot 1b156d8631fdb49a75a93e57be8eac2acb6cbbf1 (base 0eeba70): Lint, Build, Test, Bundle, Verify plist/signature, Launch smoke, Install/reinstall all ok
- epic-symbols empty; parent bob-cli-j9 stays open

## Dependencies

- **Depends on:** [bob-cli-j9.1](bob-cli-j9.1.md) ✓ · ⧖ 2026-11-09
- **Depends on:** [bob-cli-j9.2](bob-cli-j9.2.md) ✓ · ⧖ 2026-11-09
- **Blocks:** [bob-cli-j9.4](bob-cli-j9.4.md) ✓ · ⧖ 2026-11-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-j9.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-j9.3.md) | [bob-cli-j9.3](bob-cli-j9.3.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@3131414`](https://github.com/bobs-org/bob-mac-capture/commit/3131414a168c70e6df535293a935204dc252dcef) | feat(mac-capture): show typing tips on the completion-list first frame | [bob-cli-j9.3](bob-cli-j9.3.md) | 2026-11-09 14:07:35 EST |
| bob-mac-capture | [`bob-mac-capture@0eeba70`](https://github.com/bobs-org/bob-mac-capture/commit/0eeba70f86aaa3b57072e8af9a734afbc836ce4f) | fix(mac-capture): restore equals Space before the picker opens | [bob-cli-j9.3](bob-cli-j9.3.md) | 2026-11-09 14:43:42 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-j9.3--1][1] | Need the phase scope, notes, and close policy after macos-ci-check failed | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-j9.3.md

<!-- sase:referenced-by:end -->
