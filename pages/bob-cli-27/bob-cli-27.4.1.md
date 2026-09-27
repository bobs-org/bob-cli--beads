# Bead: bob-cli-27.4.1 — Reorder the adjustment notification test calls

[Bead Pages](../README.md) / [bob-cli-27.4](bob-cli-27.4.md) / bob-cli-27.4.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-27.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-27.land.md) · **Assignee:** `bob-cli-27.4.1` · **Size:** small
**Created:** 2026-09-26 20:02:59 EDT · **Closed:** 2026-09-26 20:15:41 EDT
**Plan:** [202609/fix\_mac\_adjust\_notification\_tests.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/fix_mac_adjust_notification_tests.md)

## Description

fix_calls: put relativeTarget last on the two new NotificationServiceTests capture() calls so Swift accepts them, and confirm the macOS CI test step for that commit is green.

## Notes

[2026-09-27T00:15:41Z · bob-cli-27.4.1] Reordered relativeTarget last on both pomodoro-adjust capture() calls (07cf3cb); fixed mixed-adjust preview test to assert previewResults instead of previewResult?.normalizedCaptures which is definitionally [first] (1856699). macOS CI run 36281769085 green: format, build, test (525 tests), bundle, smoke, install/reinstall all pass.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-27.4.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-27.4.1/README.md) | [bob-cli-27.4.1](bob-cli-27.4.1.md) | 0 |
