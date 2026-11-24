# Bead: bob-cli-px.5 — Bob Mac Capture shows the Mail Close Card

[Bead Pages](../README.md) / [bob-cli-px](README.md) / bob-cli-px.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1fs](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1fs.md) · **Assignee:** `bob-cli-px.5` · **Size:** medium
**Created:** 2026-11-24 12:22:30 EST · **Closed:** 2026-11-24 14:45:50 EST
**Plan:** [202611/email\_task\_close\_confirmation.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/email_task_close_confirmation.md)

## Description

mac: preview banner, a Mail Close card opened from bob's refusal, Y to confirm with the digest, and docs and CI.

## Notes

[2026-11-24T19:45:50Z · bob-cli-px.5] Mail Close Card landed: tolerant mail_close decode on previews and refusals, preview banner plus orange footer tint, refusal card keeping the draft (Y confirms via --mail-close, Cmd-Return opens gmail_url, Return hints, Esc/q/Ctrl-[ keep, second refusal refreshes, VoiceOver labels). Docs updated (capture-previews, keyboard, protocol). Verified: swift build ok, CaptureMailCloseTests 5 pass, swift test 2711 pass, docs-check pass. macOS CI run 45471925794 queued at handoff, macOS targets unverified.

## Dependencies

- **Depends on:** [bob-cli-px.2](bob-cli-px.2.md) ✓ · ⧖ 2026-11-24
- **Blocks:** [bob-cli-px.6](bob-cli-px.6.md) ◐ · ⧖ 2026-11-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-px.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-px.5/README.md) | [bob-cli-px.5](bob-cli-px.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@c2a4426`](https://github.com/bobs-org/bob-mac-capture/commit/c2a442676baa2807b117a85411ef0865c5a5923b) | feat(mac-capture)!: show the Mail Close Card for email-task closes | [bob-cli-px.5](bob-cli-px.5.md) | 2026-11-24 14:46:24 EST |
