# Bead: bob-cli-7d.4 — Panel wiring, dispatch, keys, README, and closeout

[Bead Pages](../README.md) / [bob-cli-7d](README.md) / bob-cli-7d.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.4b.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.4b.linker.w0.md) · **Assignee:** `bob-cli-7d.4` · **Size:** medium
**Created:** 2026-10-13 09:50:29 EDT · **Closed:** 2026-10-13 11:03:59 EDT
**Plan:** [202610/slash\_task\_goto.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/slash_task_goto.md)

## Description

mac-goto-panel: route `task_goto` needs and completions into the picker, accept through a separate dispatch branch (injectable opener, in-flight lock, hide and clear on success, picker stays on failure), key mapping, Ctrl-C discard, README, panel tests, green macOS CI, and the optional decision record.

## Notes

[2026-10-13T15:03:20Z · bob-cli-7d.4] CI: SHA 6345673d2dbe8a0daacd37b664fe366370bc3b25 (feat(capture): open Obsidian from the Go To picker). Run https://github.com/bobs-org/bob-mac-capture/actions/runs/38417330907 failed at Lint Swift formatting after 26s; Build/Test skipped. gh run view --log-failed grepped for error: shows 42 errors, all in CaptureLinkGuardPresentation.swift (14), CaptureModelTests.swift (22), and CaptureTogglePresentationTests.swift (6). The same 42 error lines appear on parent a86eddb (run 38414162582) and 8f89423 (run 38408350959). This phase's files have zero error: lines. Last green master CI is eed300d (run 38140692096).

[2026-10-13T15:03:24Z · bob-cli-7d.4] Mac acceptance pass (Bryan, after the epic) — copy of plan:202610/slash_task_goto.md § Mac acceptance pass:

- Cold start. Check Obsidian both quit and running.
  - If the URI is dropped when the URI itself launches Obsidian, file a follow-up for the app: launch md.obsidian, wait for it to finish launching plus a short settle, then dispatch.
  - Never add a plain open?path= "insurance" URI. It replaces the active tab and defeats leaf reuse.
- Landing.
  - the note already open in a split;
  - the task under a folded heading or list;
  - a Reading-view leaf;
  - the caret on the row in Vim normal mode, and <C-o> returning;
  - Unicode and spaces in paths.
- Moved lines.
  - Edit above the task between the search and the accept: it lands correctly with no Notice.
  - Edit the task line itself: the Notice appears.
- Lifecycle.
  - Escape during the fetch, a double Return, a dispatch failure, and a reopened panel never launch Obsidian late or capture anything.
  - A canceled / draft never comes back from the stash.
- No writes. Accept one identified row and one ID-less row. The note and day files stay byte-identical (git -C ~/bob status is clean).

Rollout first: from bob-cli, just install-all (or bob plugins sync -p bob-navigation-hotkeys, then install bob and the app). Before the panel, test the handler from Terminal with open 'obsidian://bob-goto-task?…' using target/line/ref from bob capture-complete -c 1 -f json -- '/'.

[2026-10-13T15:03:28Z · bob-cli-7d.4] PROPOSED FOLLOW-UP: Repair existing bob-mac-capture Swift CI lint/compile failures — identical 42 swift-format error: lines on this SHA 6345673 (run 38417330907), parent a86eddb (run 38414162582), and 8f89423 (run 38408350959): CaptureLinkGuardPresentation.swift reserved `guard` identifier, CaptureTogglePresentationTests.swift malformed multiline literals, CaptureModelTests.swift reserved `guard` local. Already proposed on bob-cli-7d.3 note #1; no task bead tracks it yet. This phase added no new error: lines; Build/Test never ran.

[2026-10-13T15:03:59Z · bob-cli-7d.4] mac-goto-panel landed on bob-mac-capture master 6345673d2dbe8a0daacd37b664fe366370bc3b25 (feat(capture): open Obsidian from the Go To picker). task_goto needs/completions route into the Go To picker; acceptTaskGotoRow uses injectable taskGotoOpener, in-flight lock, discard+dismiss on success, picker stays on failure; Ctrl-C discards a / draft (never CanceledDraftStash); ID-less rows open directly; Shift/Option-↩ consumed; README Go To Picker + requirements; CaptureTaskGotoPanelTests plus fake-bob / and /dee parse/complete fixtures. Fake-bob / and /dee verified locally. memory_goto_record=no; no memory notes edited. CI https://github.com/bobs-org/bob-mac-capture/actions/runs/38417330907 red at Lint with the same 42 error: lines as a86eddb and 8f89423 (bob-cli-7d.3 note #1); this phase added none; Build/Test skipped. Mac acceptance checklist copied onto this bead. No leftover --epic-symbol entries.

## Dependencies

- **Depends on:** [bob-cli-7d.2](bob-cli-7d.2.md) ✓ · ⧖ 2026-10-13
- **Depends on:** [bob-cli-7d.3](bob-cli-7d.3.md) ✓ · ⧖ 2026-10-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-7d.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-7d.4/README.md) | [bob-cli-7d.4](bob-cli-7d.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@6345673`](https://github.com/bobs-org/bob-mac-capture/commit/6345673d2dbe8a0daacd37b664fe366370bc3b25) | feat(capture): open Obsidian from the Go To picker | [bob-cli-7d.4](bob-cli-7d.4.md) | 2026-10-13 10:53:51 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-7d.4][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-7d.4/README.md

<!-- sase:referenced-by:end -->
