# Bead: bob-cli-j9.4 — The picker host for the remaining lessons

[Bead Pages](../README.md) / [bob-cli-j9](README.md) / bob-cli-j9.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.3y.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.3y.linker.w0.md) · **Assignee:** `bob-cli-j9.4` · **Size:** medium
**Created:** 2026-11-09 12:18:38 EST · **Closed:** 2026-11-09 16:11:16 EST
**Plan:** [202611/capture\_alias\_typing\_tips.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_alias_typing_tips.md)

## Description

mac-picker-tips: widen the trigger to ^ : + ~ & *, admit tips in the picker's first frame in the chosen slot, add accessibility, escapes, tests, and docs, apply the accepted memory decisions, and propose the three-week stop-rule review.

## Notes

[2026-11-09T20:57:08Z · bob-cli-j9.4] PROPOSED FOLLOW-UP: Three weeks after picker tips ship, review weekly ledger stats; keep the lessons if alias share rises, delete them otherwise, and stop immediately on any false tip.

[2026-11-09T20:59:17Z · bob-cli-j9.4] PROPOSED FOLLOW-UP: docs-check still reports the same 3 over-budget pages on the clean base (json-outputs 6143; Mac capture-panel 6006 and keyboard 6028; cap 6000); this is already recorded by bob-cli-j8.7 note #1, and bob-cli-h9 tracks the Mac page overages.

[2026-11-09T21:10:59Z · bob-cli-j9.4] PROPOSED FOLLOW-UP: Exact-SHA macOS run 42696688042 failed only at CaptureRelationEqualsAliasTests.testFastDoubleEqualsBeforeReplyCollapsesToOne (line 764; asks=1 instead of 2); this matches the existing flake task bob-cli-jb. Clean base SHA 5987de4 run 42686284282 passed.

[2026-11-09T21:11:16Z · bob-cli-j9.4] Picker alias-tip hosting, sizing, accessibility, docs, and coverage implemented. just portable-check passed 2390 tests (1 skipped). Exact-SHA run 9a2d621 lint and Build passed; 4567 macOS tests had 1 failure in the known flake bob-cli-jb, while clean base SHA 5987de4 run 42686284282 was green. docs-check failures match clean base and are recorded as follow-ups. Scratch Mac bundle attempt ended when the Mac became unreachable.

## Dependencies

- **Depends on:** [bob-cli-j9.3](bob-cli-j9.3.md) ✓ · ⧖ 2026-11-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-j9.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-j9.4/README.md) | [bob-cli-j9.4](bob-cli-j9.4.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d790681`](https://github.com/bobs-org/bob-cli/commit/d79068138e4336d6345475adafb4d880e47977d3) | docs(memory): clarify capture alias tip host | [bob-cli-j9.4](bob-cli-j9.4.md) | 2026-11-09 16:13:31 EST |
| bob-mac-capture | [`bob-mac-capture@e5833d6`](https://github.com/bobs-org/bob-mac-capture/commit/e5833d6b813ade33d8db0f73eef567c83d45fde5) | feat(capture): show alias tips in pickers | [bob-cli-j9.4](bob-cli-j9.4.md) | 2026-11-09 16:13:59 EST |
