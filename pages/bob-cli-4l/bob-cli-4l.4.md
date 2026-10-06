# Bead: bob-cli-4l.4 — Ctrl+Shift+Enter link advances from a landing

[Bead Pages](../README.md) / [bob-cli-4l](README.md) / bob-cli-4l.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.0d.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.0d.linker.w0.md) · **Assignee:** `bob-cli-4l.4` · **Size:** small
**Created:** 2026-10-06 07:01:41 EDT · **Closed:** 2026-10-06 07:31:30 EDT
**Plan:** [202610/review\_walk\_answer\_auto\_advance.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/review_walk_answer_auto_advance.md)

## Description

bip-link-today: in block-id-prompt, capture at the top of the Ctrl+Shift+Enter toggle and carry the origin on the link source through the block-ID prompt. Only a successful link continues, and its "Linked · …" text becomes the first line of the composed toast. Unlink, Work-summary unlink, prompt cancel, and failures stay (block-id-prompt 1.22.0).

## Notes

[2026-10-06T11:31:30Z · bob-cli-4l.4] block-id-prompt 1.22.0: Ctrl+Shift+Enter captures review origin, successful link continues with link-today outcome (Linked text first line of composed toast); unlink/Work-summary-unlink/cancel/failures settle null and stay. 9 new tests; full suite 1838 pass 0 fail; bob plugins sync deployed to vault

## Dependencies

- **Depends on:** [bob-cli-4l.1](bob-cli-4l.1.md) ✓ · ⧖ 2026-10-06
- **Blocks:** [bob-cli-4l.5](bob-cli-4l.5.md) ✓ · ⧖ 2026-10-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-4l.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-4l.4/README.md) | [bob-cli-4l.4](bob-cli-4l.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@0e0fb98`](https://github.com/bobs-org/bob-plugins/commit/0e0fb980ffe762233f8057f3ca784d913cff9cd6) | feat(block-id-prompt): implement bip-link-today pomodoro link-today flow | [bob-cli-4l.4](bob-cli-4l.4.md) | 2026-10-06 07:32:29 EDT |
