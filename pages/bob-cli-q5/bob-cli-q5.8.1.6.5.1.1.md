# Bead: bob-cli-q5.8.1.6.5.1.1 — Build the isolated acceptance harness and settle the CI precondition

[Bead Pages](../README.md) / [bob-cli-q5.8.1.6.5.1](bob-cli-q5.8.1.6.5.1.md) / bob-cli-q5.8.1.6.5.1.1

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.8.1.6.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.1.6.5.md) · **Assignee:** `bob-cli-q5.8.1.6.5.1.1` · **Size:** medium
**Created:** 2026-11-27 06:59:00 EST
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
| read-by | [agent:bob-cli-q5.8.1.6.5.1.1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.1.6.5.1.1.md

<!-- sase:referenced-by:end -->
