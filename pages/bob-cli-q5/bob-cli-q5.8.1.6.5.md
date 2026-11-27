# Bead: bob-cli-q5.8.1.6.5 — Accept the wake notice end to end on the real Mac

[Bead Pages](../README.md) / [bob-cli-q5.8.1.6](bob-cli-q5.8.1.6.md) / bob-cli-q5.8.1.6.5

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.8.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.1.land.md) · **Assignee:** `bob-cli-q5.8.1.6.5` · **Size:** medium
**Created:** 2026-11-26 20:05:51 EST
**Plan:** [202611/mac\_snooze\_wake\_notice\_repair.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_snooze_wake_notice_repair.md)

## Description

notice-acceptance: with a compatible bob and the built app, run the six end-to-end checks of plan:202611/mac_snooze_wake_notice.md, including a genuine human lock/unlock, fix small defects found, and record exact evidence for the land agent.

## Notes

[2026-11-27T07:47:49Z · bob-cli-q5.8.1.6.5] Acceptance preconditions checked 2026-11-27 ~02:50 EST: (1) master exact-SHA CI NOT yet green - run 45960329324 on ba213181 in_progress (macOS 26 SwiftPM job, started 07:42Z, ~20min typical). Phase .4 verified snapshot e443aa40 (run 45957005662 green) has since landed as ba213181. (2) Mac OFFLINE - tailscale ping 3/3 timeout to 100.108.201.99 plus ssh ConnectTimeout expiry; needs Bryan to bring it online. (3) bob-cli HEAD contains 3659edc0 and 59037b23; athena bob snooze -f json reports wake_notice_version 1. Mac-side bob version still unchecked. Blocked on Mac + CI; no check results recorded.

## Dependencies

- **Depends on:** [bob-cli-q5.8.1.6.4](bob-cli-q5.8.1.6.4.md) ✓ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.8.1.6.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.1.6.5.md) | [bob-cli-q5.8.1.6.5](bob-cli-q5.8.1.6.5.md) | 0 |
