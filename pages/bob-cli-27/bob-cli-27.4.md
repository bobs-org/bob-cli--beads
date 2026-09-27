# Bead: bob-cli-27.4 — Fix Mac adjustment notification test calls

[Bead Pages](../README.md) / [bob-cli-27](README.md) / bob-cli-27.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-27.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-27.land.md) · **Assignee:** `bob-cli-27.4.land`
**Created:** 2026-09-26 20:02:59 EDT · **Closed:** 2026-09-26 20:22:10 EDT
**Plan:** [202609/fix\_mac\_adjust\_notification\_tests.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/fix_mac_adjust_notification_tests.md)

## Description

bob-mac-capture's macOS CI test step compiles the Pomodoro adjustment notification tests and those tests pass.

## Notes

[2026-09-27T00:22:10Z · bob-cli-27.4.land] Verified phase bob-cli-27.4.1 and Mac commits 07cf3cb/1856699: both notification capture() calls now put relativeTarget last, and mixed adjustment preview asserts previewResults. Mac CI run 36281769085 at 1856699 passed build, 525 tests, bundle, smoke, and install/reinstall. No unrelated CLI or Mac commits landed after this child epic began, so no integration edits were needed. Child notes proposed no follow-ups; no epic-symbol entries remain. CLI just test and just lint pass; this checkout has no just check or symvision recipe.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-27.4.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-27.4.land/README.md) | [bob-cli-27.4](bob-cli-27.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli--plans | [`bob-cli--plans@c5ba4c0`](https://github.com/bobs-org/bob-cli--plans/commit/c5ba4c0e98ef1d1b04ef7061035b3b6d81fc0bbd) | docs(plans): mark Pomodoro adjustment epics done | [bob-cli-27.4](bob-cli-27.4.md) | 2026-09-26 20:24:39 EDT |
