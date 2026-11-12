# Bead: bob-cli-kq.5 — Small verified fixes

[Bead Pages](../README.md) / [bob-cli-kq](README.md) / bob-cli-kq.5

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1bo](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1bo.md) · **Assignee:** `bob-cli-kq.5` · **Size:** medium
**Created:** 2026-11-12 05:24:40 EST
**Plan:** [202611/security\_audit\_fixes\_1.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/security_audit_fixes_1.md)

## Description

small-audit-fixes: prefix-match the pomodoro OVERDUE status, close the perl two-arg open in bob_pomodoro, report damaged albums as io instead of note_changed, require FILE args on bank import, and strip migration anchors by match span.

## Notes

[2026-11-12T10:49:35Z · bob-cli-kq.5] Verified prefix OVERDUE match (Rust notify + bob_notify), perl 3-arg open in bob_pomodoro, damaged albums as io not note_changed, required FILE on bank import with empty-list refusal, and tracker complete_line strip by BLOCK_ID match span. Focused tests passed; just check staged for host close.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kq.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kq.5.md) | [bob-cli-kq.5](bob-cli-kq.5.md) | 0 |
