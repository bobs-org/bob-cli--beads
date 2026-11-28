# Bead: bob-cli-q5.8.1 — Presence-aware Mac snooze wake notices

[Bead Pages](../README.md) / [bob-cli-q5.8](bob-cli-q5.8.md) / bob-cli-q5.8.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.md) · **Assignee:** `bob-cli-q5.8.1.land`
**Created:** 2026-11-26 12:54:20 EST · **Closed:** 2026-11-28 09:27:56 EST
**Plan:** [202611/mac\_snooze\_wake\_notice.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_snooze_wake_notice.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/mac_snooze_wake_notice.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_snooze_wake_notice.md

<!-- sase:links:end -->

## Description

Complete bob-cli-q5.8 with one verified Mac wake HUD per owned batch, held during absence or meetings, actionable through Open and +15m, and backed by an automatically cleared beacon and silent Notification Center record.

## Notes

[2026-11-27T01:00:32Z · bob-cli-q5.8.1.land] LAND TRIAGE of PROPOSED FOLLOW-UPs (bob-cli-q5.8.1 land agent, 2026-11-26): (1) q5.8.1.1 #1 WISPr meeting PDF test failure still reproduces on origin/master ebc45fec -> duplicate of bob-cli-q9, +1 recorded. (2) q5.8.1.1 #1 props_contract update_json null-vs-bank assertion -> declined: passes on ebc45fec (fixed after 33fe3425). (3) q5.8.1.1 #1 stale generated plugin inventory in docs/bob-ledger-tools.md and docs/index.md -> declined: 'bob-docs gen --check' now reports the inventory up to date. (4) q5.8.1.5 #1 vault-format.md budget overrun (6030/6000) -> duplicate of closed bob-cli-oc, reproduced after its close and reopened with a verified-after-close +1. Bisected to ebc45fec (bob-cli-qm.7), so I also left a DISCOVERED ISSUE note on active epic bob-cli-qm. None of these were caused by q5.8.1.

[2026-11-27T01:04:37Z · bob-cli-q5.8.1.land] LAND VERIFICATION (bob-cli-q5.8.1 land agent, 2026-11-26): the epic is not complete. Five things block closing it. (1) bob-mac-capture master d2e9ca4a does not compile: macOS CI run 45917911039 failed in Build at StatusItemGlyph.swift:232, where 'accessibilityLabel' is initialized twice. The Mac was offline during phase .5, so the final phase never had a compile. (2) Blocking runtime defect: SnoozeNoticeCoordinator never resets the verification state after the launch probe. An active-user wake is judged against a pre-wake bob snooze read, dropped as emptyVerification or noEligibleTasks, and persisted as handled. Because bob already chose mac_capture, the desktop fallback does not fire either. (3) Contract gaps: the task day comes from the Mac clock, not bob's date/now. A failed or old-day agenda counts as no meetings. Launch presence is not sampled. The claim is not gated on observer registration, and its replace is not atomic. The vault comparison ignores symlinks. The add lane is not serialized, and bob's JSON refusal is discarded. (4) Surface gaps: no sharingType=.none. 'TODAY n/m' prints a calendar date instead of the link budget, and over-cap amber appears only as glyph color. HUD Open uses the daily Snoozed-row line with no block reference. x/timeout do not end the nudge, so restores re-present and re-post the record after a hold. Dismissal ignores the wake ID. Hover is lost on re-show. The base status glyph turns black whenever the count is above 0. The docs promise a vault-change clear that does not exist. (5) The real-Mac acceptance and genuine lock/unlock evidence were never gathered; the Mac is offline (ssh timeout). The bob-cli half (3659edc0, 59037b23) is sound and its Swift decoding matches. Integration: the only bob-cli snooze change since the epic began, ba21e4c2 (snooze-marks display docs), does not conflict; bob-mac-capture has no non-epic commits since 46c5202b. epic-symbols: none for q5.8.1 or q5.8. I proposed child epic plan sase_plan_mac_snooze_wake_notice_repair.md (parent_bead bob-cli-q5.8.1), with phases runtime-verify, runtime-facts, hud-repair, records-repair, and notice-acceptance. q5.8.1 and q5.8 stay open until it lands.

[2026-11-28T02:08:36Z · bob-cli-q5.9.1.1] BRYAN DIRECTIVE (2026-11-27): Do not ask Bryan to verify, observe, act, or answer further questions for the snooze acceptance or close-out. Replace human observation with the machine-evidence standard in plan:202611/finish_snoozed_tasks_unattended.md; record residuals where behavior cannot be proven. The nine-question round-2 gate d66607cd-82c3-48c3-ad38-3cf618c2e27f was canceled without a response by takeover phase bob-cli-q5.9.1.1.

[2026-11-28T14:27:49Z · bob-cli-q5.9.1.7] Q5.8.1 LAND (notice-land, 2026-11-28). All five implementation phases and repair epic bob-cli-q5.8.1.6 are closed. The repair epic note records commits, exact-SHA CI, docs and shell-script gates, acceptance results, and carried follow-ups. Real-Mac acceptance checks 1–6 are evidenced in q5.9.1.5/q5.9.1.6 and consolidated under q5.8.1.6.5.1; the acceptance-only harness has been removed and production integrity is verified.

[2026-11-28T14:27:56Z · bob-cli-q5.9.1.7] All implementation and repair phases closed; q5.8 acceptance evidence, CI/docs gates, teardown, and production check recorded.

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.8.1.2][1] | Need parent epic scope and plan path | 1 |
| read-by | [agent:bob-cli-q5.8.1.4--1][2] | Need the epic decisions and phase requirements after the exact-SHA test failure | 1 |
| read-by | [agent:bob-cli-q5.8.1.5][3] | Need epic scope for records phase | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.8.1.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.1.4.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.8.1.5/README.md

<!-- sase:referenced-by:end -->
