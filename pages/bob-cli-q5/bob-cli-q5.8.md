# Bead: bob-cli-q5.8 — Presence-aware wake notice on the Mac

[Bead Pages](../README.md) / [bob-cli-q5](README.md) / bob-cli-q5.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1fx](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1fx.md) · **Assignee:** `bob-cli-q5.8` · **Size:** large
**Created:** 2026-11-25 10:22:53 EST · **Closed:** 2026-11-28 09:27:56 EST
**Plan:** [202611/snoozed\_tasks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/snoozed_tasks.md)

## Description

mac-wake-notice: the notifier claim file, snooze-woken receipt observer, pure presence and meeting hold policy, the wake notice surface with chime and +15m, the menu-bar beacon, the silent Notification Center record with withdrawal, Settings, and Mac docs.

## Notes

[2026-11-26T17:53:01Z · bob-cli-q5.8] Planning only; no product files changed. Confirmed q5.7 landed through bob-mac-capture 46c5202b and q5.8 has no prior implementation. Prepared a validated five-phase child epic (protocol, portable policy, runtime, HUD, records/settings). Necessary protocol findings: snooze receipts are posted for all notification modes without channel ownership; History/list state woken does not establish current task eligibility; receipt daily_file is vault-relative. Plan adds compatible authority/revalidation fields before activating the Mac observer. epic-symbols currently clean. Child land owns compiled/CI/manual lock-unlock evidence and q5.8 closure; outer q5 remains open.

[2026-11-28T02:08:41Z · bob-cli-q5.9.1.1] BRYAN DIRECTIVE (2026-11-27): Do not ask Bryan to verify, observe, act, or answer further questions for the snooze acceptance or close-out. Replace human observation with the machine-evidence standard in plan:202611/finish_snoozed_tasks_unattended.md; record residuals where behavior cannot be proven. The nine-question round-2 gate d66607cd-82c3-48c3-ad38-3cf618c2e27f was canceled without a response by takeover phase bob-cli-q5.9.1.1.

[2026-11-28T14:28:21Z · bob-cli-q5.9.1.7] Q5.8 LAND EVIDENCE (notice-land, 2026-11-28). The q5.8.1 implementation and repair epics are closed. Product acceptance SHA 84506599514cff20f0351ae5d31b6f8938bea04 passed exact-SHA macOS CI run 46100086357; earlier exact gates 45932873351, 45948302176, and 45957005662 are recorded on the repair phases. Current harness/docs SHA 5bda4cc3 passed just docs-check (449 passed, 1 skipped; all implemented gates green) and just check-scripts (43 checks). Acceptance checks 1–6 have machine evidence and residuals in q5.9.1.5/q5.9.1.6, consolidated at q5.8.1.6.5.1. The harness down command returned leftover=none; production remains live from ~/Applications with matching notifier claim PID 46053, no bobDirectory override, and no harness slugs under ~/bob. Notice-land carries untriaged follow-ups.

## Dependencies

- **Depends on:** [bob-cli-q5.7](bob-cli-q5.7.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q5.9](bob-cli-q5.9.md) ✓ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.md) | [bob-cli-q5.8](bob-cli-q5.8.md) | 0 |
