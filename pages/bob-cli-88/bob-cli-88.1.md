# Bead: bob-cli-88.1 — bob-navigation-hotkeys deletes emptied entries on every cleanup

[Bead Pages](../README.md) / [bob-cli-88](README.md) / bob-cli-88.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase · **↺ Reopened:** ↺1
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.10m](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.10m.md) · **Assignee:** `bob-cli-88.1` · **Size:** medium
**Created:** 2026-10-16 07:28:58 EDT · **Closed:** 2026-10-16 08:14:07 EDT
**Plan:** [202610/emptied\_pomodoro\_cleanup.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/emptied_pomodoro_cleanup.md)

## Previously Closed

> ↺ Closed 2026-10-16T11:52:40Z · done
>
> (none)
>
> Reopened 2026-10-16T11:56:26Z by a status update

## Description

nav: make planDeferredPomodoroLinkCleanup always delete emptied open entries, retire the removeEmptiedEntries flag, align its dedicated-bullet check, and cover Alt+N release, Task Card cancel, single and Task Link schedule/priority, and link-roll paths with tests.

## Notes

[2026-10-16T11:51:49Z · bob-cli-88.1] PROPOSED FOLLOW-UP: Fix the six full-suite failures reproduced unchanged on clean base — four unblocked-glyph cases (bob-cli-6v), the Keep notice test (bob-cli-6w), and reverse-conversion BLOCKS re-keying (bob-cli-7i).

[2026-10-16T11:52:40Z · bob-cli-88.1] Implemented and built bob-navigation-hotkeys 2.41.0; focused cleanup/keymap tests passed 188/188; deployed the plugin. Full npm test has six failures reproduced on clean base and tracked by bob-cli-6v, bob-cli-6w, and bob-cli-7i; recorded as proposed follow-up. epic-symbols check found none.

[2026-10-16T11:56:26Z · bryanbugyi34@gmail.com] I'm not sure if this work is completed or not but the agent that was attempting to work on it failed.

[2026-10-16T12:11:01Z · bob-cli-88.1] PROPOSED FOLLOW-UP: Standing cleanup decision record skipped — epic decision_record=no forbids editing the decisions web; land agent should retain or triage this explicitly deferred memory change.

[2026-10-16T12:11:05Z · bob-cli-88.1] PROPOSED FOLLOW-UP: Corroborated the six existing full-suite failures on clean bob-plugins base 5205c3a before edits — four unblocked-glyph failures (bob-cli-6v), Keep notice (bob-cli-6w), and reverse-conversion BLOCKS re-keying (bob-cli-7i). Their failure messages reproduce unchanged after this phase; no new task beads created.

[2026-10-16T12:14:07Z · bob-cli-88.1] Completed nav cleanup in bob-plugins 2.41.0: unconditional emptied-open-entry deletion; decorated dedicated-link cleanup; correct link/entry counts, fenced-child handling, blank seams, EOF/CRLF, cursor mapping and single-write undo behavior. Build and manifest validation passed; 200 focused tests passed. Final npm test: 2846/2852 pass, with all six failure signatures exactly matching clean base 5205c3a (bob-cli-6v, bob-cli-6w, bob-cli-7i), recorded as proposed follow-up. Deployed only bob-navigation-hotkeys and confirmed synced; no epic-symbol entries remain. No memory notes edited; skipped decision record noted. Parent epic left open.

## Dependencies

- **Blocks:** [bob-cli-88.4](bob-cli-88.4.md) ◐ · ⧖ 2026-10-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-88.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-88.1/README.md) | [bob-cli-88.1](bob-cli-88.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@86cebc9`](https://github.com/bobs-org/bob-plugins/commit/86cebc9c4dcf83a238b387127b5eedf8c68f9725) | feat(bob-navigation-hotkeys): delete Pomodoros emptied by every cleanup | [bob-cli-88.1](bob-cli-88.1.md) | 2026-10-16 08:14:53 EDT |
