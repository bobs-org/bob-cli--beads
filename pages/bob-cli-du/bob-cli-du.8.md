# Bead: bob-cli-du.8 — Bob Mac Capture renders bob's complete consequences and offers

[Bead Pages](../README.md) / [bob-cli-du](README.md) / bob-cli-du.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.aw](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.aw.md) · **Assignee:** `bob-cli-du.8` · **Size:** medium
**Created:** 2026-10-28 14:49:53 EDT · **Closed:** 2026-10-28 20:39:13 EDT
**Plan:** [202610/relation\_complete\_labels.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/relation_complete_labels.md)

## Description

mac-complete-cue: generalize the cancel cue into one close-effect presentation, decode the complete fields, render the ✓ capsule, sentence, slot, span tint, preview rows, and submit hint, and feed complete-label offers into the in-panel successor choice.

## Notes

[2026-10-29T00:39:13Z · bob-cli-du.8] mac-complete-cue done in linked bob-mac-capture. Verified: CaptureCore decodes completes_source/relation_complete/relation_completes[]/complete_effect/relation_completed_source with old-bob tolerance; RelationSourceEffect generalizes the 5 cancel hooks with cancel UI pixel-identical (CaptureRelationCancelTests still green); card renders checkmark.circle completes capsule, dimmed '✓ S' sentence, bob's slot message per verdict (completes/already_closed/recurring/new_task/inverse hint), Completes-VoiceOver; draft completes_source spans take the green complete role; preview adds ✓ message plus ! transition/ledger/unblocked rows under the 🪢 row with no duplicate warning; submit hints Capture & complete N / Capture & close N; relation_completes[].taskComplete.unblocked feeds makePullInPreviewSnapshot so the in-panel successor choice opens like !. Tests: new CaptureRelationCompleteTests (11, incl. 10 real-bob fixtures from generate-relation-complete-fixtures.sh with 2-unblocked/1-offer commit) + 4 new CaptureRelationPanelTests card/submit cases; full portable suite 1741 tests 0 failures on athena (swift 6.0.3); docs-check passed (447 passed). NOT verified (mac offline per tailnet): BobMacCapture app-target typecheck (typecheck-tests.sh), macOS CI, light/dark screenshots — app files syntax-checked only; needs a mac pass before rollout.

## Dependencies

- **Depends on:** [bob-cli-du.3](bob-cli-du.3.md) ✓ · ⧖ 2026-10-28
- **Blocks:** [bob-cli-du.9](bob-cli-du.9.md) ◐ · ⧖ 2026-10-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-du.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-du.8/README.md) | [bob-cli-du.8](bob-cli-du.8.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@072055d`](https://github.com/bobs-org/bob-mac-capture/commit/072055d01fea3f6e5e212b177f42f540d32f995b) | feat(mac-capture): render bob's complete-label consequences and offers | [bob-cli-du.8](bob-cli-du.8.md) | 2026-10-28 20:48:58 EDT |
