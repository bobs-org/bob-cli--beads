# Bead: bob-cli-q5.8.1.6.1 — Restore the build and verify each wake against a fresh bob read

[Bead Pages](../README.md) / [bob-cli-q5.8.1.6](bob-cli-q5.8.1.6.md) / bob-cli-q5.8.1.6.1

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.8.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.1.land.md) · **Assignee:** `bob-cli-q5.8.1.6.1` · **Size:** medium
**Created:** 2026-11-26 20:05:50 EST
**Plan:** [202611/mac\_snooze\_wake\_notice\_repair.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_snooze_wake_notice_repair.md)

## Description

runtime-verify: fix the StatusItemGlyph build break, make every accepted receipt verify against a bob snooze read started after it, deliver immediately when nothing held, gate and atomically publish the notifier claim, and make the snooze process lanes serialize writes, surface bob refusals, and never cancel each other.

## Dependencies

- **Blocks:** [bob-cli-q5.8.1.6.2](bob-cli-q5.8.1.6.2.md) ◐ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.8.1.6.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.1.6.1.md) | [bob-cli-q5.8.1.6.1](bob-cli-q5.8.1.6.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@d2294ec`](https://github.com/bobs-org/bob-mac-capture/commit/d2294eca0e2e64c01e86cc44039b6ae3903e6540) | fix(snooze): verify wake notices against fresh state | [bob-cli-q5.8.1.6.1](bob-cli-q5.8.1.6.1.md) | 2026-11-26 20:48:23 EST |
