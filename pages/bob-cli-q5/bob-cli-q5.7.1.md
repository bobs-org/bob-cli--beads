# Bead: bob-cli-q5.7.1 — Mac snoozed agenda and always-on wake scheduler

[Bead Pages](../README.md) / [bob-cli-q5.7](bob-cli-q5.7.md) / bob-cli-q5.7.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.7.md) · **Assignee:** `bob-cli-q5.7.1.land`
**Created:** 2026-11-26 07:49:18 EST · **Closed:** 2026-11-26 12:44:22 EST
**Plan:** [202611/mac\_snoozed\_agenda.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_snoozed_agenda.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/mac_snoozed_agenda.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_snoozed_agenda.md

<!-- sase:links:end -->

## Description

Complete bob-cli-q5.7: show snoozed tasks separately in the Mac agenda, preserve their summary under folding, mark fresh wakes, and run Bob's wake writer at its advertised instant while the panel is hidden.

## Notes

[2026-11-26T15:54:38Z · bob-cli-q5.7.1.land] LAND AUDIT / FOLLOW-UP TRIAGE (2026-11-26): Read this epic, every child and every note (.1 notes 1-2, .2 notes 1-4, .3 note 1), source phase bob-cli-q5.7, both linked plans, and decisions:mac-capture-is-a-thin-client, decisions:idle-capture-shows-ledger-agenda, decisions:today-is-read-from-the-ledger. Reviewed Mac commits c4a30591, e387187f, e4a97f52, a4a7020d and current models, fixtures, editor span mapping, presentation/folding/measurement/views, process client, app/store lifecycle, policy/scheduler, and tests. The four agenda-snoozed fixtures exactly match bob-cli. All additive decoding, budget/numbering separation, first-fold summary, accent expiry, +5-second timing, and non-cancelling writer wiring are present. Earlier compile/layout/countdown concerns are resolved: GitHub run 45847440694 succeeded in lint/build/test/bundle/signature/launch/install; fetched snapshot f923059807e9efa942476d1a51bb7388d26c9efe and current Mac a4a7020d have identical tree b52b21dbc584c2217c5613fe0aa06f9c4dbb8189. Phase .3 reports 2837 portable tests (one skip), scratch bundle/typecheck, and docs-check; this lander independently confirmed CI steps and tree equality, not a fresh full-suite run. Integration: Mac master/origin master a4a7020d; bob-cli master/origin master 4dd787bc. Non-epic Mac commits since first epic commit are aa233750/38dc0dee, and creation-time drift also includes 6ea5b8f6; bob-cli drift is 4dd787bc. They repair true-case drawer fixtures/assertions, do not add competing agenda/wake consumers, and need no extra feature integration. PROPOSED FOLLOW-UP from bob-cli-q5.7.1.2 note 1 (CapturePlaceMenuPresentationTests.testEmptyQueryOpensWithOnThisTaskAndRecentGroupsAndNothingSelected: 3 vs 4 weeks ago) DECLINED AS RESOLVED: aa233750 replaces the real-date literal with Bob-returned detail and stable prefix/suffix, 38dc0dee unwraps optional detail; both are in the verified green tree. Used sase_new_task; searched CI then all task types across statuses, swept last-week task beads, inspected active epic scopes and bob-cli-ph. No duplicate task needed and no defect remains to attach as active work. The only proposed follow-up is fully triaged. No --epic-symbol entries for bob-cli-q5.7.1. Epic remains open for scheduler/summary repairs described in the next note.

[2026-11-26T15:54:44Z · bob-cli-q5.7.1.land] REMAINING EPIC WORK: (1) CaptureSnoozeWakePolicy.settle clears target/retryDeadline on nil or a new target, but SnoozeWakeScheduler.refreshScheduleFromSnapshot re-applies its retained old snapshot on every timer/lifecycle callback. Executed the unmodified production CaptureSnoozeWake.swift with minimal DTO stubs: update old 2026-08-28T09:00:00-04:00 at target+5; beginAttempt true; settle nil (and separately 19:00 target) at +1; update same snapshot at +2; beginAttempt returned true in both cases. This violates retirement and the 60-second retry floor. (2) finishWakeAttempt treats deferred/skipped exactly like woke; nil next_wake_at disarms, and byte-identical CaptureAgendaStore refresh publishes nothing, so due work can lose all retries. Real bob-cli wake_report (src/native/snooze/cli.rs) computes next_wake_at from a prospective postimage when the plan has woken rows even on deferred/skipped paths, so these replies do not prove a write happened. Preserve due retries for non-writing outcomes until fresh agenda facts retire them. Also guard in-flight results across day/executable changes and pin unsupported-command cache entries to the identity that launched the process (current snoozeWake catch writes identityToken again). Add realistic fake-Bob/policy regressions; existing tests only cover deferred with the SAME non-null target. (3) CaptureAgendaRowView .snoozedSummary passes literal "alarm " into CaptureAgendaChipButton, whose body is Text(text). Replace it with the intended SF Symbol alarm and recheck rendered heights/light-dark evidence. These are caused by this epic, not standalone follow-ups. A medium tale will finish these changes, required compilation/CI, then close this epic and parent phase bob-cli-q5.7 normally; it must leave outer epic bob-cli-q5 open.

[2026-11-26T16:27:23Z · bob-cli-q5.7.1.land--1] DISCOVERED FLAKE bob-cli-qk: MeetingNotesSessionTests.testOutOfOrderPreviewCannotReplaceNewEventSelection failed 1/2846 in full portable-check on 46c5202b, passed on isolated rerun; all snooze/scheduler/process-client tests green. Filed as flake, unrelated to this epic's scope.

[2026-11-26T17:44:22Z · bob-cli-q5.7.1.land--4] Landing complete on Mac 46c5202bfeda51757088e645dd04dc21db1f53a6 == origin/master clean, bob-cli untouched/clean. Scope: additive snoozed/woke_at decoding, snooze-span tint, Later-today dim band after strip with first-fold persistent summary (alarm N later, next HH:MM), separate budget alarm N, 60-min fresh-woke accents, hidden-panel +5s non-cancelling snooze-wake lane with bounded 60s retries, day/clock/lifecycle invalidation. Repairs: wake-outcome provenance retained through callbacks (null stays retired, future stays scheduled), deferred/skipped treated as non-writing with preserved retry deadline, unsupported-command cache pinned to launching identity, folded summary renders SF Symbol alarm not literal text. Drift integrated: Mac aa233750/38dc0dee (drawer time-robustness), 6ea5b8f6; bob-cli 4dd787bc; no competing agenda/wake consumers. Verification: just portable-check 2846 tests 1 skip PASS; scratch Mac Scripts/bundle.sh + just typecheck-tests PASS; prior CI 45847440694 tree-equal b52b21db; authoritative precommit gate 9ntrn9ejrj7d exit 0 on snapshot 40f15ef41c85c63cd7eeb6c4b8e0bd8ceff252ac, run https://github.com/bobs-org/bob-mac-capture/actions/runs/45865004175 (lint/build/test/bundle/signature/launch/install all ok); prior gate necjhh3w9t2r exit 2 was gh rate-limit/auth infra, not a CI verdict. Follow-up: bob-cli-q5.7.1.2 note-1 place-menu 3-vs-4-weeks-ago DECLINED AS RESOLVED (fixed by aa233750/38dc0dee in green tree); flake bob-cli-qk MeetingNotesSessionTests out-of-order preview 1/2846 filed separately, rerun green. epic-symbols clean.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.7.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.7.1.land.md) | [bob-cli-q5.7.1](bob-cli-q5.7.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@46c5202`](https://github.com/bobs-org/bob-mac-capture/commit/46c5202bfeda51757088e645dd04dc21db1f53a6) | fix(capture): preserve wake outcome provenance and bounded retries, render folded alarm icon | [bob-cli-q5.7.1](bob-cli-q5.7.1.md) | 2026-11-26 11:20:28 EST |
| bob-cli--plans | [`bob-cli--plans@d928866`](https://github.com/bobs-org/bob-cli--plans/commit/d9288663bba8ea4a363cc8ae7f5078de5b7c38e0) | docs(plans): mark mac snoozed agenda done | [bob-cli-q5.7.1](bob-cli-q5.7.1.md) | 2026-11-26 12:46:05 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.7.1.1][1] | need parent epic scope and design | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.7.1.1/README.md

<!-- sase:referenced-by:end -->
