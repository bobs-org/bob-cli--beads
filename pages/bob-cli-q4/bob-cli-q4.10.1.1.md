# Bead: bob-cli-q4.10.1.1 — Navigation settle adapter, command flush, and identity mapping

[Bead Pages](../README.md) / [bob-cli-q4.10.1](bob-cli-q4.10.1.md) / bob-cli-q4.10.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q4.10](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q4.10.md) · **Assignee:** `bob-cli-q4.10.1.1` · **Size:** medium
**Created:** 2026-11-25 14:29:10 EST · **Closed:** 2026-11-25 14:56:20 EST
**Plan:** [202611/navigation\_gesture\_settle.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/navigation_gesture_settle.md)

## Description

settle-bridge: add a guarded nav consumer of taskSettle v1, reusable editor and file-postimage preparation, command-entry flushing, and identity/line-map forwarding for nav state and jumps. Preserve annotated transactions and exact rollback writes. Add focused adapter, command-route, cursor, and walk-identity tests.

## Notes

[2026-11-25T19:54:22Z · bob-cli-q4.10.1.1] Settle-bridge landed in bob-navigation-hotkeys 2.107.6 (deployed, no -F). Guarded consumer of ledger-tools taskSettle v1: applyNavSettledEditorWrite / AnnotatedWrite / RestoreWrite / prepareNavSettledFilePostimage. Missing/old/throwing provider falls back to the existing gesture; stale preimage and A-to-B path/view refuse without writing; restore never settles. applyEditorContentTransaction is not an unconditional settle hook.

FLUSH ROUTES
- commands: onload installNavTaskSettleCommandFlush wraps registered bob-navigation-hotkeys:* callback/editorCallback; checkCallback/editorCheckCallback only when checking !== true (docs-inventory forbids aliasing addCommand, so wrapping is registry-based like ledger-tools)
- vim: registerVimMappings defineAction wrappers for toggle pin, jump back, jump forward
- physical (after chord/mode, before count/cursor): handleOpenTaskJumpPhysicalKeydown, handleCountedBulletPropertyPhysicalKeydown, handleCountedLaneTogglePhysicalKeydown, handleCountedTransclusionTogglePhysicalKeydown, handleCountedTaskMovePhysicalKeydown, handleReviewRefreshPhysicalKeydown, handleTaskSplitPhysicalKeydown, handlePomodoroSplitPhysicalKeydown
- publicApi: reviewWalk.capture, claimReviewWalkCompletion, openDependencyStage, removeDependency, openFileInActiveLeaf
- skipped: checkCallback when checking === true; arbitrary typing / every keydown; recordJump; review-refresh held-key tracking at start of handleReviewRefreshPhysicalKeydown

Identity: unique blockId is authoritative; disappeared/duplicate IDs do not fall back to a stale line number. Queue/resume/jump maps compose with settle lineMap. Cursor stay records one jump.

Verified: npm test (9572 pass / 4 skip / 0 fail + 26 perf); 22 new adapter/command/identity tests including real taskSettle v1 AREA fixture.

[2026-11-25T19:56:20Z · bob-cli-q4.10.1.1] settle-bridge landed in bob-navigation-hotkeys 2.107.6 (deployed without -F). Guarded taskSettle v1 consumer: applyNavSettledEditorWrite/AnnotatedWrite/RestoreWrite and prepareNavSettledFilePostimage; missing/old/throwing provider keeps the existing gesture; stale preimage and A-to-B path/view refuse; restore writes exact recorded bytes. applyEditorContentTransaction is not an unconditional settle hook. Command flush wraps registered bob-navigation-hotkeys:* callbacks at end of onload (docs-inventory forbids addCommand alias); Vim defineAction wrappers; physical routes flush after chord/mode before count/cursor; public APIs flush on capture/claim/openDependency/removeDependency/openFileInActiveLeaf. Identity: unique blockId is authoritative; disappeared/duplicate IDs do not fall back to a stale line. npm test: 9572 pass / 4 skip / 0 fail + 26 perf; 22 new adapter/command/identity tests. No leftover --epic-symbol entries.

## Dependencies

- **Blocks:** [bob-cli-q4.10.1.2](bob-cli-q4.10.1.2.md) ◐ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q4.10.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.10.1.1/README.md) | [bob-cli-q4.10.1.1](bob-cli-q4.10.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@f224bc7`](https://github.com/bobs-org/bob-plugins/commit/f224bc725d29b6402e8e537f9b69cc6c2dc61aa6) | feat(nav): add guarded taskSettle v1 consumer and command flush | [bob-cli-q4.10.1.1](bob-cli-q4.10.1.1.md) | 2026-11-25 15:03:41 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q4.10.1.1][1] | Need the phase scope and design file | 5 |
| read-by | [agent:bob-cli-q4.9.1.1][2] | Need q4.10.1.1 scope because it currently holds the cycler vault deploy | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.10.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.9.1.1/README.md

<!-- sase:referenced-by:end -->
