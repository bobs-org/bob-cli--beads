# Bead: bob-cli-q5.9.1.7 — Tear down the harness and land the q5.8 subtree

[Bead Pages](../README.md) / [bob-cli-q5.9.1](bob-cli-q5.9.1.md) / bob-cli-q5.9.1.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1hl](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1hl.md) · **Assignee:** `bob-cli-q5.9.1.7` · **Size:** small
**Created:** 2026-11-27 20:55:09 EST · **Closed:** 2026-11-28 09:28:46 EST
**Plan:** [202611/finish\_snoozed\_tasks\_unattended.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_snoozed_tasks_unattended.md)

## Description

notice-land: tear down the harness and confirm production is intact. Write the per-check evidence and close the open q5.8 beads bottom-up, carrying their untriaged follow-ups forward.

## Notes

[2026-11-28T14:21:51Z · bob-cli-q5.9.1.7] PROPOSED FOLLOW-UP: Rerun the check-3 three-task mutation sequence with a driver that targets woken [*] rows and verifies the documented drop refusal, then clarify the planned disappearance expectation. Source: bob-cli-q5.9.1.5 note #2.

[2026-11-28T14:21:56Z · bob-cli-q5.9.1.7] PROPOSED FOLLOW-UP: Fix the acceptance noauth variant so it publishes its own claim, then complete the denial wake check. Source: bob-cli-q5.9.1.5 notes #2–3.

[2026-11-28T14:22:02Z · bob-cli-q5.9.1.7] PROPOSED FOLLOW-UP: Correct SnoozeWakePresenceSource.liveInitialState console-state lookup: current source still checks kCGSessionOnConsoleKey, while the observed session dictionary key is kCGSSessionOnConsoleKey. Add a test for an off-console launch. Source: bob-cli-q5.8.1.6.5.1.1 note #46.

[2026-11-28T14:22:08Z · bob-cli-q5.9.1.7] PROPOSED FOLLOW-UP: Investigate the previously reported production notifier claim loss after install-all restarts and the held-receipt capability-probe starvation; current production claim was live at teardown, but that does not verify restart behavior. Sources: bob-cli-q5.8.1.6.5.1.1 notes #38 and #42.

[2026-11-28T14:22:13Z · bob-cli-q5.9.1.7] PROPOSED FOLLOW-UP: Profile first SnoozeWakeHUD presentation; earlier signposts suggested synchronous display/record work blocked the main thread for about 2.2 seconds. Source: bob-cli-q5.8.1.6.5.1.1 note #62.

[2026-11-28T14:22:19Z · bob-cli-q5.9.1.7] PROPOSED FOLLOW-UP: Triage the CaptureTaskGotoPanelTests.testLateFailureAfterChipReopenSuccessHasNoEffect flake (red once, green on rerun); no task bead was recorded as tracking it. Source: bob-cli-q5.8.1.6.5.1.1 note #5.

[2026-11-28T14:22:24Z · bob-cli-q5.9.1.7] PROPOSED FOLLOW-UP: Triage the MeetingNotesSessionTests out-of-order selection/list flakes, including testOutOfOrderPreviewCannotReplaceNewEventSelection and testLateListCannotReplaceNewerChooserGeneration. Related existing task bob-cli-qk is cited in bob-cli-q5.8.1.6.4 note #1; source findings also appear in bob-cli-q5.8.1.6.5.1.1 note #15 and bob-cli-q5.8.1.6.2 note #1.

[2026-11-28T14:22:30Z · bob-cli-q5.9.1.7] PROPOSED FOLLOW-UP: Reconcile the baseline docs/reference/vault-format.md word-budget overrun (6030/6000); existing task bob-cli-oc tracks the issue. Source: bob-cli-q5.8.1.6.4 note #2.

[2026-11-28T14:28:46Z · bob-cli-q5.9.1.7] q5.8 subtree closed bottom-up; scratch harness teardown returned leftover=none; production PID and claim 46053 remain live from ~/Applications with no bobDirectory override or harness slugs; docs-check and check-scripts passed; acceptance residuals and untriaged follow-ups recorded.

## Dependencies

- **Depends on:** [bob-cli-q5.9.1.6](bob-cli-q5.9.1.6.md) ✓ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.9.1.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.9.1.7/README.md) | [bob-cli-q5.9.1.7](bob-cli-q5.9.1.7.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:1hm--code][1] | Check waiting notice-land phase before continuing the q5 chain | 1 |
| read-by | [agent:bob-cli-q5.9.1.9][2] | Cite Mac half of cases 1 and 8 from mac-accept/lock-accept for e2e | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1hm.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.9.1.9/README.md

<!-- sase:referenced-by:end -->
