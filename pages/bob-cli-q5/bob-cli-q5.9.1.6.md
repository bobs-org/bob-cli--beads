# Bead: bob-cli-q5.9.1.6 — Accept check 2 from a natural lock and Bryan's own unlock

[Bead Pages](../README.md) / [bob-cli-q5.9.1](bob-cli-q5.9.1.md) / bob-cli-q5.9.1.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1hl](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1hl.md) · **Assignee:** `bob-cli-q5.9.1.6` · **Size:** small
**Created:** 2026-11-27 20:55:09 EST · **Closed:** 2026-11-28 09:04:45 EST
**Plan:** [202611/finish\_snoozed\_tasks\_unattended.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_snoozed_tasks_unattended.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:433542f4fe0cb521743b6b2a | attached via sase artifact create --bead |
| related | file:explicit:9d14fb7053155b79725bf562 | attached via sase artifact create --bead |
| related | file:explicit:afcc1777e4931612ebb9d783 | attached via sase artifact create --bead |
| related | file:explicit:c3cb6280016494952f93cb7a | attached via sase artifact create --bead |
| related | file:explicit:e2cec44d8f1ea517fae4d2c5 | attached via sase artifact create --bead |
| related | file:explicit:e35680140de3fb3f96134724 | attached via sase artifact create --bead |
| related | file:explicit:ea42da6d8e398ed9862add8d | attached via sase artifact create --bead |
| related | file:explicit:f96fcf5e05d4fc31d3437179 | attached via sase artifact create --bead |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

lock-accept: arm the lock watcher and wait passively, with an idle-gated display-sleep fallback, for a real lock and unlock. Prove the locked wake stayed silent and surfaced after unlock.

## Notes

[2026-11-28T04:13:50Z · bob-cli-q5.9.1.6] lock-accept ARMED and HOLDING (interim, check not yet passed): set snoozeWakeHoldWhileAway on via probe set (real reconfigure path; hold-during-meetings already on). App SHA 84506599514cff20f0351ae5d31b6f8938bea04, exact-SHA CI 46100086357 green, Mac bob 0.6.0. guard ok (prod 70216, scratch 29025). Screen was already locked on first check 23:06 (genuine: Bryan-owned lock; we never lock). lockwatch PID 55152 (pid file corrected; first two starts died in guard because my own lingering starter SSH session added a second pgrep -f bob-wake-accept/ match at the 10s guard - restarted with short-lived session, guard passed; follow-up: keep starter sessions short-lived). Wake 18ec1a1fef29d208-0-55926 Lock check 1 (test, no action needed) held at lock_seconds 10. Held snapshots: coordinator held, hold_reason away(screenLocked), HUD visible false, no chime, no announcement, no new record (delivered still the 2 old IDs), frontmost loginwindow. Silent hold proven live; unlock/pass pending. Adapter tests at probe SHA: SnoozeWakePresenceSourceTests testIdleThresholdBoundary, testLaunchingWithDisplayAsleepHolds, testLaunchingWithInactiveSessionHolds, testScreenLockHoldsUntilUnlock, testDisplaySleepAndSessionSignalsHoldIndependently, testIdlePollingRunsOnlyWhileHeld + SnoozeWakeNoticePolicyTests testEachAwaySignalHoldsIndependently. -r Record lock-accept interim silent-hold evidence

[2026-11-28T12:50:41Z · 1hm--code] Takeover: this tale owns the remaining lock-accept work under plan:202611/finish_q5_lock_accept.md. The overnight watcher proved the silent hold, then both queued receipts aged out at four hours before Bryan's 06:04 unlock; no unlock delivery could be observed. Root causes for the retry: lockwatch lacks expiry/midnight refresh; its guard fails after production PID changed 70216→43460; find_scratch_pids treats SSH command lines containing the harness root as scratch processes; Amphetamine holds PreventUserIdleDisplaySleep so the idle accelerator cannot fire (natural locks remain the path). The old monitor gnaxy21893qm was stopped with no successor; recorded lockwatch PID 55152 was confirmed and stopped while scratch app 29025 and signpost stream 29151 remain running. No step will ask Bryan to act or observe.

[2026-11-28T13:16:34Z · 1hm--code] Interim next_lock setup. The prior lockwatch log has 415 lines and records the genuine 23:06 lock, silent hold for wake 18ec1a1fef29d208-0-55926, the c3m3 receipt, two four-hour expiries, midnight reset, and 06:04 unlock after both receipts had left the queue. Persisted signpost retrieval produced only its header; the saved stream contains PID 29025 snooze-hold, snooze-verify, and day-purge events. Local copies are /tmp/q5-lock-accept/lockwatch-run-1.log and /tmp/q5-lock-accept/signposts-stream.log for attachment in final evidence. Harness changes in bob-mac-capture are complete: script SHA e4df510e971bec3111983944c5f2d09a470b7758cd7344892e077369dc09efa8; just check-scripts passed (43 tests) and just docs-check passed (449 passed, 1 skipped). Deployed the script. The production app restarted twice during takeover; adopt refreshed only harness files after the four checks, ending with production PID 80522. Scratch app 83667 runs app SHA 84506599514cff20f0351ae5d31b6f8938bea04 (CI 46100086357 green); Mac bob 0.6.0; announce, chime, hold-while-away, and hold-during-meetings are on. Bob and probe snapshots both showed an empty scratch queue. Current lockwatch PID is 9318; timestamped waiting-lock began at 2026-11-28T08:07:50-05:00. No production process or vault was changed.

[2026-11-28T14:04:16Z · 1hm--1] LOCK-ACCEPT FINAL — check 2 passed under unlock_wait=next_lock.

A natural lock caused by Bryan's own lock, followed by his own unlock, held one scratch wake silently and presented it exactly once after unlock. The pass was collected by lockwatch at 2026-11-28 08:48:04 EST; no simulated lock was used.

Harness and app evidence:
- Scratch app SHA: 84506599514cff20f0351ae5d31b6f8938bea04; exact-SHA CI run 46100086357 passed.
- Deployed harness script SHA: e4df510e971bec3111983944c5f2d09a470b7758cd7344892e077369dc09efa8. Exact-SHA CI run 46149096720 passed for source SHA 5bda4cc3b5837df7d6a3ab536753649fafb2639c; the monitor verified the deployed script hash matched.
- Mac bob: 0.6.0.
- Before evidence collection the recorded production PID 29408 was stale. `adopt` verified one live production PID (46053), its notifier claim, no production bobDirectory, and zero test-task marker files; adopt and both surrounding guards passed. No production process or vault was written, killed, or relaunched.

Passing wake 18ec388d04e62890-0-47461:
- Lock: 2026-11-28T08:28:35-05:00. Wake/held: 08:28:50-05:00. It remained queued with `away(screenLocked)` through the held snapshots.
- Unlock: 2026-11-28T08:48:01-05:00. Pass snapshot: 08:48:04-05:00, after 1.5 seconds settling. No expiry, rollover, or refresh was needed during this 20-minute hold.
- Signposts: 222 `snooze-hold` entries for this wake with `reason=away(screenLocked)`; one `snooze-return` at 08:47:55.898, one `snooze-verify` at 08:47:57.460, one `snooze-present` at 08:47:57.503, and one `snooze-record` at 08:48:00.345. The exported signpost file contains exactly one present and one record for this wake.
- Passing probe snapshot seq 608: coordinator `presenting`, `pending_count=0`, delivered contains this wake; HUD visible with the same wake ID; announcement “Ready now · Lock check 1 (test, no action needed)”; chime played; exactly one `snooze-woken-18ec388d04e62890-0-47461` delivered record. The live HUD PNG and full JSON snapshot are attached.
- Lockwatch logged `phase=pass`, then `phase=exit, code=0`. Signpost export ran between passing guards after safe PID adoption.

Deterministic adapter coverage (seven tests):
- SnoozeWakePresenceSourceTests: `testIdleThresholdBoundary`, `testLaunchingWithDisplayAsleepHolds`, `testLaunchingWithInactiveSessionHolds`, `testScreenLockHoldsUntilUnlock`, `testDisplaySleepAndSessionSignalsHoldIndependently`, `testIdlePollingRunsOnlyWhileHeld`.
- SnoozeWakeNoticePolicyTests: `testEachAwaySignalHoldsIndependently`.

Last-night supporting evidence remains attached: wake 18ec1a1fef29d208-0-55926 was silently held under `away(screenLocked)` from the genuine 23:06 lock; wake 18ec1aa92c43ac48-0-2027 joined at about 23:21. At midnight the daily handled list reset. Their receipts aged out at the four-hour limit around 03:11 and 03:21 while still held, so Bryan's 06:04 unlock had nothing pending and the old lockwatch recorded `unlock-timeout`. The previous signpost stream and 415-line lockwatch log are attached as supporting evidence; this harness gap was fixed by the deployed expiry/midnight refresh handling and the successful next-lock run above.

Attachments are the current lockwatch log, full signposts since lock, signpost event excerpt, passing JSON snapshot and HUD PNG, plus last-night lockwatch/signpost logs and excerpt.

Attached SASE evidence refs:
- `file:explicit:ea42da6d8e398ed9862add8d` — current lockwatch run 2 log.
- `file:explicit:433542f4fe0cb521743b6b2a` — full run 2 signposts since lock.
- `file:explicit:c3cb6280016494952f93cb7a` — current signpost event excerpt.
- `file:explicit:afcc1777e4931612ebb9d783` — passing probe snapshot seq 608.
- `file:explicit:9d14fb7053155b79725bf562` — passing HUD PNG.
- `file:explicit:f96fcf5e05d4fc31d3437179` — last-night lockwatch run 1 log.
- `file:explicit:e2cec44d8f1ea517fae4d2c5` — last-night signpost stream.
- `file:explicit:e35680140de3fb3f96134724` — last-night signpost event excerpt.

[2026-11-28T14:04:45Z · 1hm--1] Check 2 passed on the natural lock and unlock; final note #4 contains the complete evidence and eight durable attachments. epic-symbols was empty.

## Dependencies

- **Depends on:** [bob-cli-q5.9.1.5](bob-cli-q5.9.1.5.md) ✓ · ⧖ 2026-11-27
- **Blocks:** [bob-cli-q5.9.1.7](bob-cli-q5.9.1.7.md) ✓ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.9.1.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.9.1.6.md) | [bob-cli-q5.9.1.6](bob-cli-q5.9.1.6.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:1hm--code][1] | Inspect the interim note after a quoting mistake and correct its record | 2 |
| read-by | [agent:bob-cli-q5.9.1.9][2] | Cite Mac half of cases 1 and 8 from mac-accept/lock-accept for e2e | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1hm.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.9.1.9/README.md

<!-- sase:referenced-by:end -->
