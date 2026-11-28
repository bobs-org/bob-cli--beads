# Bead: bob-cli-q5.9.1 — Finish Snoozed Tasks without asking Bryan to verify anything

[Bead Pages](../README.md) / [bob-cli-q5.9](bob-cli-q5.9.md) / bob-cli-q5.9.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1hl](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1hl.md) · **Assignee:** `bob-cli-q5.9.1.land`
**Created:** 2026-11-27 20:55:07 EST · **Closed:** 2026-11-28 09:52:59 EST
**Plan:** [202611/finish\_snoozed\_tasks\_unattended.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_snoozed_tasks_unattended.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/finish_snoozed_tasks_unattended.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_snoozed_tasks_unattended.md

<!-- sase:links:end -->

## Description

bob-cli-q5.9 closes, leaving bob-cli-q5 ready for its waiting land agent. The stalled human-observation flow is retired, and the four q5-owned discovered issues are fixed. The Mac wake notice is proven on the real Mac from in-app machine evidence and a natural lock and unlock. The q5.8 subtree is landed. The glossary strand, guide, and live end-to-end acceptance ship. No question, prompt, or observation is asked of Bryan.

## Notes

[2026-11-28T02:08:52Z · bob-cli-q5.9.1.1] BRYAN DIRECTIVE (2026-11-27): Do not ask Bryan to verify, observe, act, or answer further questions for the snooze acceptance or close-out. Replace human observation with the machine-evidence standard in plan:202611/finish_snoozed_tasks_unattended.md; record residuals where behavior cannot be proven. The nine-question round-2 gate d66607cd-82c3-48c3-ad38-3cf618c2e27f was canceled without a response by takeover phase bob-cli-q5.9.1.1.

[2026-11-28T14:52:59Z · bob-cli-q5.9.1.land] Land verified (bob-cli-q5.9.1.land, 2026-11-28).

STEP 1, VERIFY: all 9 phases are closed and every phase note was addressed.
- takeover (.1): round-2 gate canceled with no answers; driver 82289 stopped; stale waiters killed; directive recorded.
- bob-fixes (.2): commit 684811a9. Read the per-verb deferred_add_report/deferred_drop_report code and its three shape tests. Rounding is now worded as the delta rule. Grammar 34 is claimed in compatibility.md and capture.md, with Grammar 33/34 history.
- plugin-resnooze (.3): bob-plugins b23ccaee. Read snoozeMutationUpsertRow against Rust upsert_active_row; vectors pass 21/21.
- mac-probe (.4): bob-mac-capture 84506599, CI 46100086357 green. The probe gate is the .accept prefix plus the default, with testProductionIdentityNeverEnablesTheProbe. Every test name cited in the acceptance notes exists.
- mac-accept (.5) and lock-accept (.6): machine evidence for checks 1 and 3-6, and a natural lock/unlock pass for check 2. Wake 18ec388d04e62890-0-47461 had exactly one present and one record. The harness hardening is 5bda4cc3, CI 46149096720.
- notice-land (.7): the q5.8 subtree is closed (q5.8 confirmed CLOSED). Teardown left nothing behind, and production PID 46053 still holds its claim.
- closeout-docs (.8): 21eb1cce. glossary:snoozed-task, the docs/guides/snooze-task-for-later-today.md guide, the concepts paragraph, and nav entries.
- e2e (.9): CLI cases 1-7, marks 66/67, card 60/60.
The DECISIONS are honored. Only glossary:snoozed-task was edited (memory diff of 21eb1cce); decision_record=no held; uncommitted_rows=ignore wording is in the strand.

LANDER FIX: the JS planner retime dropped the old active Snoozed row's notes when live-link notes were consumed. Rust keeps both; reproduced with bob 0.6.0 in a scratch vault against the planner harness. Fixed in bob-plugins 738-snooze-mutation-planner.js (always carry the active children after the consumed notes) with a new planner test.
- Checks: npm run build, build:check, all 15 snooze test files (165/165), vectors 21/21, docs:check.
- Full npm test: 10480 pass, 1 fail (bob-cli-rq: cabinets-chrome, fails identically on the clean base).
- Deployed with bob plugins sync -p bob-navigation-hotkeys. Committed with this landing.

STEP 2, INTEGRATE: reviewed every commit after the epic started.
- bob-cli: 518b29fe, 08165ed9, f561ebd0, 0aa33a49.
- bob-plugins: d0ddd12c, a6f7691e, 301da199, d55ba760, d3e748a6.
- bob-mac-capture: 6c545f23.
None touches snooze code or contracts (the only snooze strings are fixture text), so nothing needed to adopt or deconflict the epic's additions. The regenerated AGENTS.md and glossary pages keep the Snoozed Task entry.

STEP 3, FOLLOW-UP TRIAGE:
- .2 #1 ref_library ratio flake: +1 on bob-cli-hr.
- .3 #2 'ranker cpu clock' seam-test flake: +1 on bob-cli-3w, which reopened to READY as a regression of the n5.5 fix.
- .9 #3 reading-tomato-regression: +1 on bob-cli-qs (a deterministic Reading-view defect, not a midnight flake).
- .7 #7 MeetingNotes flakes: +1 on bob-cli-qk, adding testLateListCannotReplaceNewerChooserGeneration and the 6c545f23 hint.
- .7 #2 and #4, noauth claim plus claim loss after restart: recorded as one DISCOVERED ISSUE on bob-cli-q5, caused by q5.8. Root cause confirmed in source: the .hold branch cancels the capability-probe fetch.
- .7 #3 console key: DISCOVERED ISSUE on bob-cli-q5.
- .7 #5 HUD main-thread stall: DISCOVERED ISSUE on bob-cli-q5, corroborated by the 2.8 s present-to-record gap in .6.
- .7 #6 Go To panel flake: new task bob-cli-rw (flake, ready).
- Lander-found cabinets-chrome failure: +1 on bob-cli-rq.

DECLINED:
- .5 #2 / .7 #1, check-3 triple rerun: the harness is torn down and check 3 is proven by the held-then-released sweep batch. The drop refusal on woken rows is by design (plan_drop removes only unstruck active rows). Tests cover the paths: testFreshReadWithoutReceiptRowsDropsAndHandlesTheBatch, testMeetingHoldDelaysUntilRealEnd, testOverlappingMeetingsHoldPastFirstEnd.
- .7 #8 vault-format word budget: bob-cli-oc is closed, and the page is 5992/6000 words on master.
- .6 #1 and #2 lockwatch/guard/scratch-pid harness gaps: fixed by 5bda4cc3. Amphetamine's display-sleep assertion is environmental, and natural locks were the path.

epic-symbols is empty for q5.9.1 and q5.9.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.9.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.9.1.land/README.md) | [bob-cli-q5.9.1](bob-cli-q5.9.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@1d5595b`](https://github.com/bobs-org/bob-plugins/commit/1d5595b734f2047f5b172fa51f0dde583e4bae0c) | fix(snooze): keep active Snoozed row notes when a retime consumes live-link notes | [bob-cli-q5.9.1](bob-cli-q5.9.1.md) | 2026-11-28 09:59:11 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:1hm--code][1] | Check phase state and chain for lock-accept completion | 1 |
| read-by | [agent:bob-cli-q5.9.1.9][2] | Need parent epic plan and DECISIONS for e2e phase | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1hm.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.9.1.9/README.md

<!-- sase:referenced-by:end -->
