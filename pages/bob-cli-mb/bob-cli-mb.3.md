# Bead: bob-cli-mb.3 — Mac: Recent group in the empty \`//\` picker from an app-local open log

[Bead Pages](../README.md) / [bob-cli-mb](README.md) / bob-cli-mb.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1cs](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1cs.md) · **Assignee:** `bob-cli-mb.3` · **Size:** medium
**Created:** 2026-11-16 10:14:22 EST · **Closed:** 2026-11-16 11:41:20 EST
**Plan:** [202611/note\_goto\_followups.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/note_goto_followups.md)

## Description

mac-recent-notes: record each successful `//` open in an app-local, schema-versioned open log, show up to eight recently opened notes as a Recent section after Today in the empty Notes picker, add a Settings action that clears the log, and land green on macOS CI.

## Notes

[2026-11-16T15:39:14Z · bob-cli-mb.3] Recent group implemented: NoteGotoOpenLogStore (app-local, FNV vault hash, 500/365d prune, 0600/0700, quarantine), Recent section in NoteGotoPickerIndex (after Today, max 8, recent: IDs, filtered unchanged), model records on success-only and feeds warm-swap/chip paths, Settings Go To Notes clear button, docs go-to-notes/settings. Verified: just portable-check 2537 tests 0 failures, just docs-check 447 passed. Remaining: macOS typecheck-tests scratch compile, macos-ci-check precommit gate, master exact-SHA CI to green.

[2026-11-16T16:41:05Z · bob-cli-mb.3--2] Recent-group master CI green on rerun: SHA 61d29a6f3c1978ca78067e235ce98938344d8bf1, run https://github.com/bobs-org/bob-mac-capture/actions/runs/43899389310 (conclusion success after rerun of failed jobs)

[2026-11-16T16:41:20Z · bob-cli-mb.3--2] Verified Recent-group empty-// picker work landed on master 61d29a6f and green: just portable-check 2537 tests 0 failures, just docs-check 447 passed, Scripts/macos-ci-check exit 0, exact-SHA master CI run 43899389310 conclusion success on rerun (https://github.com/bobs-org/bob-mac-capture/actions/runs/43899389310). First attempt hit one flaky timing failure in CaptureDotRouteAliasTests.testFastDoubleDotBeforeReplyCollapsesToOne (fake-bob rewrite count with 0.4s delay), unrelated to Recent-group diff which touches only NoteGoto open log, picker presentation, panel model, and Settings. epic-symbols empty.

## Dependencies

- **Blocks:** [bob-cli-mb.4](bob-cli-mb.4.md) ✓ · ⧖ 2026-11-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-mb.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-mb.3.md) | [bob-cli-mb.3](bob-cli-mb.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@61d29a6`](https://github.com/bobs-org/bob-mac-capture/commit/61d29a6f3c1978ca78067e235ce98938344d8bf1) | feat(capture): show recently opened notes in the // empty state | [bob-cli-mb.3](bob-cli-mb.3.md) | 2026-11-16 10:43:01 EST |
