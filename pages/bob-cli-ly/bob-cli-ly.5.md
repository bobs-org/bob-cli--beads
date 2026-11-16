# Bead: bob-cli-ly.5 — No-blink scope swap, warm notes snapshot, accessibility, closeout

[Bead Pages](../README.md) / [bob-cli-ly](README.md) / bob-cli-ly.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1cr](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1cr.md) · **Assignee:** `bob-cli-ly.5` · **Size:** medium
**Created:** 2026-11-15 16:47:01 EST · **Closed:** 2026-11-16 09:12:22 EST
**Plan:** [202611/note\_goto\_double\_slash.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/note_goto_double_slash.md)

## Description

mac-note-polish: keep the card mounted across `/` and `//`, serve rows from a warm in-memory snapshot, announce scope changes, run the acceptance closeout, and write the decision strand only when its memory decision says yes.

## Notes

[2026-11-16T13:14:57Z · bob-cli-ly.5] CLOSEOUT (mac-note-polish, commit df08e6f5): card stays mounted across / and // via GotoScopeSwapState (no teardown in continue/peel; budget+selection carried; real response completes+announces, stale presents retire the swap); warm NoteGotoSnapshotStore (fill on first / session, panel show, debounced vault watcher; trust=note_goto context only; never persisted/logged); Loading notes placeholder on empty store; Could not load notes failure card; 120ms ease-out rows+capsule cross-fade, instant under Reduce Motion. Verified: portable-check 2520 tests 0 failures (8 new store tests); mac scratch bundle+typecheck-tests PASS (5 new panel tests); mac docs-check PASS with BOB_CLI_DIR=workspace. PROPOSED FOLLOW-UP: land docs/_meta/search_smoke.yml // double-slash entry (uncommitted in bob-cli workspace) so bob-cli just docs-check and cached-master gates go green; until the train ships it, mac CI docs-check via cached bob-cli master stays red on test_every_capture_token... (pre-existing epic straggler, fails identically on clean base). PROPOSED FOLLOW-UP: task-pickers.md sits at 5999/6000 reference words; next edit must trim or move content to go-to-notes.md. BRYAN MAC CHECKLIST: fast // race <350ms; backslash-then-slash vs double-backslash; open note keeps caret/scroll/Reading mode in split, background tab, Reading view; vault git status clean after opening notes; spaces/unicode/# /& paths; duplicate basenames distinguishable; old-bob Update hint.

[2026-11-16T13:46:42Z · bob-cli-ly.5] CI FOLLOW-UP run 43873762164 (df08e6f5): Test failed with 9 failures, all mine. Root causes: (1) handleCompletionResponse dismisses every non-record completion while any picker is mounted, so swap analyses never presented (4 timeouts). (2) warm prefetch fired on every taskGoto present, breaking 3 exact-count pins. Fix commit 898b8215: swap-aware dismissal bypass plus prefetch gated to fresh session opens; exact-count pins updated to the specified prefetch contract. Watching run 43878959418.

[2026-11-16T14:12:07Z · bob-cli-ly.5] VERIFIED EXACT SHA 898b8215: macOS CI run https://github.com/bobs-org/bob-mac-capture/actions/runs/43878959418 completed success — lint, build, full test suite (incl. 5 new NoteGoto panel tests + 8 store tests), bundle, plist/signature, launch smoke, install/reinstall all green. Linked checkout clean at 898b8215. epic-symbols empty.

[2026-11-16T14:12:22Z · bob-cli-ly.5] mac-note-polish complete and verified: mounted / ⇄ // swap, warm snapshot, loading/failure cards, scope announcements, Reduce Motion cross-fade, docs, exact-SHA macOS CI 43878959418 green on 898b8215. Follow-ups on bead: land bob-cli search_smoke // entry; task-pickers.md at 5999/6000 words; Bryan Mac acceptance checklist.

## Dependencies

- **Depends on:** [bob-cli-ly.4](bob-cli-ly.4.md) ✓ · ⧖ 2026-11-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ly.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ly.5/README.md) | [bob-cli-ly.5](bob-cli-ly.5.md) | 3 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@df08e6f`](https://github.com/bobs-org/bob-mac-capture/commit/df08e6f56fbed7c0a7c944bfa793c7ffdbe2f685) | feat(capture): keep Go To mounted across / and // with a warm notes snapshot | [bob-cli-ly.5](bob-cli-ly.5.md) | 2026-11-16 08:13:39 EST |
| bob-mac-capture | [`bob-mac-capture@898b821`](https://github.com/bobs-org/bob-mac-capture/commit/898b8215fb6d2b4714a549ed55dd77b5ad1c266e) | fix(capture): route swap responses past the mounted-picker dismissal | [bob-cli-ly.5](bob-cli-ly.5.md) | 2026-11-16 08:46:05 EST |
| bob-cli | [`122c7fc`](https://github.com/bobs-org/bob-cli/commit/122c7fcf9b501ccc7ba8c1b4c9113e0454e5b9d0) | docs(search): add // scope entry to search smoke | [bob-cli-ly.5](bob-cli-ly.5.md) | 2026-11-16 09:15:36 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ly.5][1] | Need the phase scope and design file | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ly.5/README.md

<!-- sase:referenced-by:end -->
