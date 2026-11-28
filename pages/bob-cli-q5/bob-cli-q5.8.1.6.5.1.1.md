# Bead: bob-cli-q5.8.1.6.5.1.1 — Build the isolated acceptance harness and settle the CI precondition

[Bead Pages](../README.md) / [bob-cli-q5.8.1.6.5.1](bob-cli-q5.8.1.6.5.1.md) / bob-cli-q5.8.1.6.5.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.8.1.6.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.1.6.5.md) · **Assignee:** `bob-cli-q5.8.1.6.5.1.1` · **Size:** medium
**Created:** 2026-11-27 06:59:00 EST · **Closed:** 2026-11-27 17:14:59 EST
**Plan:** [202611/mac\_wake\_notice\_acceptance.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_wake_notice_acceptance.md)

## Description

harness: settle master exact-SHA CI for ba213181, then build a scratch Bob Mac Capture with its own bundle ID, defaults domain, disabled hotkeys, XDG state, disposable vault, signpost evidence log, production guard, and teardown, prove one wake end to end through signposts, and get its notification permission granted.

## Notes

[2026-11-27T12:28:21Z · bob-cli-q5.8.1.6.5.1.1--1] Gate 2026-11-27T12:24:49Z answers verbatim: Q1 Mac present -> selected [Yes, active and unlocked]; Q2 permission/hotkey -> selected [Other] with custom_feedback: "I am not seeing any Bob Mac Capture Accept application on my machine and I am not sure where to go when I get to System Settings."

[2026-11-27T12:28:25Z · bob-cli-q5.8.1.6.5.1.1--1] CI update 2026-11-27 ~07:28 EST: rerun 45960329324 attempt 2 on ba213181 is now green (completed 12:20:58Z, all steps success including Test). Confirms prior single-test failure was flake. New master SHA 2253dec0 (harness script commit) CI run 45997437603 in_progress started 12:17:49Z; smoke wake must wait for its green per plan rule that any newer master SHA be green.

[2026-11-27T13:05:35Z · bob-cli-q5.8.1.6.5.1.1--2] Gate 2026-11-27T13:02:50Z answers verbatim: Q3 Accept-app Settings -> selected [Other] with custom_feedback: "I can't scroll the settings panel that opens up. I already have another agent working on fixing this but it seems like we're going to need to use the system settings for now."; Q4 Hotkey -> selected [Production opened] (Ctrl-Shift-Cmd-I still opens production Bob Mac Capture panel).

[2026-11-27T13:05:58Z · bob-cli-q5.8.1.6.5.1.1--2] CI update 2026-11-27 ~08:05 EST: master 2253dec0 (harness script commit) CI run 45997437603 is green (macOS 26 SwiftPM 27m8s, completed). Precondition now holds for latest master; harness running ba213181 is stale and must be rebuilt from 2253dec0 before the smoke wake.

[2026-11-27T13:06:05Z · bob-cli-q5.8.1.6.5.1.1--2] PROPOSED FOLLOW-UP: CaptureTaskGotoPanelTests.testLateFailureAfterChipReopenSuccessHasNoEffect flaked once on ba213181 rerun 45960329324 attempt 1, green on attempt 2 (completed 12:20:58Z) — no open task bead tracks CaptureTaskGotoPanelTests flakes.

[2026-11-27T13:11:54Z · bob-cli-q5.8.1.6.5.1.1--2] Harness rebuilt 2026-11-27 ~08:12 EST: down clean (leftover none), up from master 2253dec0ae519fb9c0f358fcd4ada2781bbffec2 (CI 45997437603 green, dirty false). guard ok:true, status clean. NOTE: production restarted mid-rebuild (old PID 39430 gone, new PID 61688 from ~/Applications with live claim started_at 2026-11-27T13:09:26Z); guard confirms new PID + claim, prod domain has no bobDirectory. Scratch PID 99735 with live accept claim started_at 2026-11-27T13:11:21Z; accept domain holds only bobDirectory + 4 disabled hotkeys. Signpost stream alive; no snooze- lines yet (no wake run). Harness left running for permission + smoke wake.

[2026-11-27T14:03:22Z · bob-cli-q5.8.1.6.5.1.1--3] Gate 2026-11-27T13:58:02Z answers verbatim: Q5 Notify-perm -> selected [Not listed] (no Bob Mac Capture Accept entry under System Settings > Notifications); Q6 Accept-setup -> selected [Other] with custom_feedback: "The settings panel scroll is fixed, but not for the scratch app. I could not see the section you were talking about."

[2026-11-27T14:03:31Z · bob-cli-q5.8.1.6.5.1.1--3] Harness repair 2026-11-27 ~09:03 EST: both PIDs went stale at ~08:52-08:55 EST. Production 61688 -> 98514 (cmdline carries --bob-mac-capture-install-restart; claim live naming 98514 started 13:52:50Z). Scratch 99735 -> 14542 (self restart-requested signpost 08:55:11; env XDG_STATE_HOME/BOB_DIR intact; accept claim live naming 14542 started 13:55:13Z). Production domain had gained bobDirectory="" (empty, recorded state at 06:51 EST was absent); deleted the key to restore recorded state, verified ~/bob has no harness seed and daily notes intact. Re-adopted recorded PIDs (98514/14542), restarted signpost stream for 14542, guard ok:true (both claims match PIDs, prod domain clean). Harness bytes still green-SHA 2253dec0 (CI 45997437603 success). Rebuild to f0285549 (scroll fix) waits on CI 46009975677, in_progress at 14:03Z.

[2026-11-27T14:05:09Z · bob-cli-q5.8.1.6.5.1.1--3] Re-check 2026-11-27 ~09:06 EST: guard still ok:true (prod 98514, scratch 14542, both claims match, prod domain clean). CI 46009975677 on f0285549 still in_progress (~19m in); rebuild to scroll-fix SHA waits on green. Monitor cyct9b still watching.

[2026-11-27T14:08:07Z · bob-cli-q5.8.1.6.5.1.1--3] CI 46009975677 attempt 1 on f0285549 is RED (completed ~14:07Z): Test step failed, xctest exited with signal 11 (SIGSEGV) at 14:06:19Z, 0.7s after new test SettingsScrollContainerTests/testHandleKeyDownPassesThroughForAnotherWindow started. All earlier steps (scripts, lint, build) green. Crash sits in a test added by the scroll-fix commit itself, so rebuild is BLOCKED (plan: newer master SHA must be green). Requested failed-jobs rerun ~14:08Z to separate flake from real breakage; if attempt 2 fails the same way this belongs to the settings-scroll agent, not this harness phase.

[2026-11-27T14:09:24Z · bob-cli-q5.8.1.6.5.1.1--3] Guard failed again 2026-11-27 ~09:09 EST: recorded production PID 98514 dead. Production restarted itself at 14:06:22Z as PID 6370, again with --bob-mac-capture-install-restart flag; claim live naming 6370, prod domain still has no bobDirectory, scratch 14542 and signpost stream untouched. Third production restart today (39430->61688 ~08:12, 61688->98514 ~08:52, 98514->6370 ~09:06). Re-adopted recorded PID to 6370 after verifying claim+domain; guard ok:true. Cause of repeated installer restarts unknown; asking Bryan now.

[2026-11-27T14:09:44Z · bob-cli-q5.8.1.6.5.1.1--3] NEXT ROUND: ask Bryan what keeps restarting production (3 installer-flag restarts ~08:12/~08:52/~09:06 EST today). Could not stage the question this turn: a pending handoff (.sase_handoff_staged.json, the CI watcher) already exists. Batch it with the post-rebuild permission round: (1) production restart cause, (2) Enable Notifications + Send Test Notification in rebuilt Accept Settings, (3) Ctrl-Shift-Cmd-I hotkey check. Then smoke wake while active.

[2026-11-27T14:27:26Z · bob-cli-q5.8.1.6.5.1.1] Guard failed 2026-11-27 ~09:26 EST: production PID 6370 dead. Production restarted at 09:23:48 EST as PID 35292 (--bob-mac-capture-install-restart), and ~/Applications/Bob Mac Capture.app/Contents/MacOS/BobMacCapture mtime is 09:23, so an outside `just install` caused it (4th today: ~08:12, ~08:52, ~09:06, ~09:23). The harness did not cause it. Verified the claim names 35292 (app org.bobs.bob-mac-capture, started 14:23:49Z), the prod domain has no bobDirectory, and ~/bob/jobs.md has no harness slugs. Re-adopted production.pid=35292; guard ok:true (scratch 14542 claim matches). Harness still on 2253dec0; waiting for CI 46009975677 attempt 2 on f0285549.

[2026-11-27T15:11:51Z · bob-cli-q5.8.1.6.5.1.1] CI 2026-11-27 ~09:28 EST: master f0285549 (settings scroll fix, agent 1h0, now finished) CI 46009975677 attempt 2 is RED the same way as attempt 1: xctest SIGSEGV (signal 11) at 14:27:33Z, 0.8s after SettingsScrollContainerTests/testHandleKeyDownPassesThroughForAnotherWindow started. It is deterministic, not a flake. Cause: the test builds a second NSWindow ("other") without isReleasedWhenClosed=false, so other.close() in defer frees it and ARC frees it again (over-release). The sibling sheet test has the same pattern. Every other test window in the suite sets the flag. Fix (test-only, 2 lines): set isReleasedWhenClosed=false on other and sheet in Tests/BobMacCaptureTests/SettingsScrollContainerTests.swift. Verified: Mac scratch-copy bundle.sh exit 0 + just typecheck-tests PASS (copy deleted); Scripts/macos-ci-check run 46018198478 on snapshot bcbfcd1e is all green (Lint, Build, Test, Bundle, plist/signature, launch smoke, install/reinstall). The fix lands on master at this turn end; the harness rebuild waits on that exact-SHA master CI.

[2026-11-27T15:11:58Z · bob-cli-q5.8.1.6.5.1.1] PROPOSED FOLLOW-UP: MeetingNotesSessionTests.testOutOfOrderPreviewCannotReplaceNewEventSelection (CaptureCoreTests) is flaky on athena Linux: failed 6/10 runs of swift test --filter MeetingNotesSessionTests at bob-mac-capture f0285549 (ordering assert [new, old] vs [old, new]), and it makes just portable-check red. Unrelated to this epic: Linux never compiles the macOS-only BobMacCaptureTests target. No open task bead tracks it.

[2026-11-27T15:12:02Z · bob-cli-q5.8.1.6.5.1.1] PROPOSED FOLLOW-UP: production Bob Mac Capture was reinstalled from outside the harness 4 times today (~08:12, ~08:52, ~09:06, ~09:23 EST; each with --bob-mac-capture-install-restart), and each one fails guard on the production-PID check, so it has to be re-adopted by hand. Consider a guard/adopt mode that accepts a new ~/Applications PID when the claim names it, the bundle mtime is newer, and the prod domain is clean. This needs a script change plus CI, so it is out of scope here.

[2026-11-27T15:13:35Z · bob-cli-q5.8.1.6.5.1.1] NEXT ROUND (2026-11-27 ~10:13 EST): the SettingsScrollContainerTests fix lands on bob-mac-capture master at this turn end, and monitor m0brg8 watches that exact-SHA master CI. On green, the successor guards and re-adopts if needed, rebuilds the harness from the new SHA (down, git archive to /tmp/harness-src, up --sha), then asks Bryan one round: Enable Notifications + Send Test Notification in the Accept Settings, the Ctrl-Shift-Cmd-I production hotkey check, and the cause of the production reinstalls. Then it runs the smoke wake. The Mac was offline (SSH timeout) at ~10:10 EST; the last guard was ok:true at ~09:27 EST (prod 35292, scratch 14542).

[2026-11-27T15:36:13Z · bob-cli-q5.8.1.6.5.1.1--1] CI 2026-11-27 ~10:35 EST: master 4053b19e (SettingsScrollContainerTests over-release fix) CI 46023087406 attempt 1 is RED, but not from the fix. All 7 SettingsScrollContainerTests tests pass, there is no crash, and the suite ran to the end (5539 tests, 5 failures across 2 tests). The two failures are known timing flakes: (1) CaptureRelatedLaneTests.testRapidEditsAreDebouncedAndTheSettingSuppressesTheLane got 2 capture-related calls, not 1 (lines 88/94), tracked by bob-cli-hu; (2) CaptureAliasTipPanelTests.testEditingTheSigilAfterItShowsClearsTheTipRow timed out waiting for the tip

… and 51011 more characters

## Dependencies

- **Blocks:** [bob-cli-q5.8.1.6.5.1.2](bob-cli-q5.8.1.6.5.1.2.md) ◐ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.8.1.6.5.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.1.6.5.1.1.md) | [bob-cli-q5.8.1.6.5.1.1](bob-cli-q5.8.1.6.5.1.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:1h9--code][1] | Check harness phase ownership before touching harness | 2 |
| read-by | [agent:bob-cli-q5.8.1.6.5.1.1][2] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-q5.8.1.6.5.1.1--8][2] | Need phase scope, design, and latest notes to continue after Bryan's Held-reason answers | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1h9.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.1.6.5.1.1.md

<!-- sase:referenced-by:end -->
