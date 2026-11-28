# Bead: bob-cli-q5.8.1.6.5.1 — Finish the Mac wake notice acceptance on an isolated harness

[Bead Pages](../README.md) / [bob-cli-q5.8.1.6.5](bob-cli-q5.8.1.6.5.md) / bob-cli-q5.8.1.6.5.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.8.1.6.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.1.6.5.md) · **Assignee:** `bob-cli-q5.8.1.6.5.1.land`
**Created:** 2026-11-27 06:59:00 EST · **Closed:** 2026-11-28 09:19:35 EST
**Plan:** [202611/mac\_wake\_notice\_acceptance.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_wake_notice_acceptance.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/mac_wake_notice_acceptance.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_wake_notice_acceptance.md

<!-- sase:links:end -->

## Description

Close bob-cli-q5.8.1.6.5 by running the six end-to-end wake-notice checks on the real Mac against a scratch app that has its own bundle ID, defaults domain, hotkey, state, and vault, so production Bob Mac Capture is never disturbed again, and by recording durable per-check evidence.

## Notes

[2026-11-27T12:16:37Z · bob-cli-q5.8.1.6.5.1.1] CI precondition 2026-11-27 ~07:25 EST: rerun 45960329324 attempt 2 on ba213181 still in_progress (Test step, ~30min in). Parent SHA 586d9ccb master run 45948197667 is green. ba213181 diff touches only SnoozeWake/Beacon/Glyph/docs + AppDelegate/NotificationService wake path (16 files); CaptureTaskGotoPanelTests file untouched. PROPOSED FOLLOW-UP: if attempt 2 fails the same single test (testLateFailureAfterChipReopenSuccessHasNoEffect, Optional(8) vs Optional(3) timeout), treat as flake/pre-existing, not wake-caused. No open task bead tracks that test; parent bead bob-cli-q5.8.1.6.5 note 6 already records it.

[2026-11-27T12:16:47Z · bob-cli-q5.8.1.6.5.1.1] Harness up+guard green 2026-11-27 ~07:20 EST. Scripts/snooze-accept.sh committed-branch per harness_home=commit (sha256 3c99d10f1786914b129639190bd9606d3f55dc6e3e2943d26c1f3a8451109884, wired into justfile docs-test bash -n; just check-scripts exit 0 on athena; shellcheck clean). Mac /tmp/harness-src = git-archive ba213181 + identical script bytes. up --sha ba213181: bundle built, ad-hoc signed, bundle ID org.bobs.bob-mac-capture.accept verified via PlistBuddy; accept domain seeded (bobDirectory=/tmp/bob-wake-accept/vault, all four hotkeys false); vault confirm: wake_notice_version 1 + realpath vault_root match. Scratch PID 28630 with XDG_STATE_HOME+BOB_DIR env verified via ps -E; claim app org.bobs.bob-mac-capture.accept pid 28630 live; signpost stream alive; guard ok:true. Production PID recorded 39430 (was 65214 at 07:04; changed independently, harness only reads it); production claim pid 39430 live; production domain has no bobDirectory. Harness left running for delivery. Next: Q1 permission+hotkey, then wake smoketest1 while Bryan active, then Q2 observations.

[2026-11-28T02:08:21Z · bob-cli-q5.9.1.1] BRYAN DIRECTIVE (2026-11-27): Do not ask Bryan to verify, observe, act, or answer further questions for the snooze acceptance or close-out. Replace human observation with the machine-evidence standard in plan:202611/finish_snoozed_tasks_unattended.md; record residuals where behavior cannot be proven. The nine-question round-2 gate d66607cd-82c3-48c3-ad38-3cf618c2e27f was canceled without a response by takeover phase bob-cli-q5.9.1.1.

[2026-11-28T14:19:35Z · bob-cli-q5.9.1.7] All four child phases closed; checks 1–6 consolidated with machine evidence, tests, residuals, and production teardown verification.

[2026-11-28T14:20:11Z · bob-cli-q5.9.1.7] CONSOLIDATED ACCEPTANCE (notice-land, 2026-11-28). The four child phases are closed. Checks 1, 3–6 machine evidence is in bob-cli-q5.9.1.5 notes #2–3 (app SHA 84506599514cff20f0351ae5d31b6f8938bea04, exact-SHA CI 46100086357); check 2 evidence is in bob-cli-q5.9.1.6 notes #4–5 (natural lock/unlock, wake 18ec388d04e62890-0-47461, 222 silent hold signposts, one return/present/record, passing snapshot seq 608 and attached artifacts). Probe snapshots, signposts, deterministic tests, and render-fixture inspection replace the prior observation requirement per the directive. Tests and residuals are itemized on child phases and q5.9.1.5. Follow-ups carried on notice-land. Harness torn down; final production checks passed (live PID/claim 46053 under ~/Applications, no production bobDirectory, no harness slugs).

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.8.1.6.5.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.8.1.6.5.1.land/README.md) | [bob-cli-q5.8.1.6.5.1](bob-cli-q5.8.1.6.5.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.8.1.6.5.1.1][1] | Need parent epic scope and plan | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.1.6.5.1.1.md

<!-- sase:referenced-by:end -->
