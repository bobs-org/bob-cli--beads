# Bead: bob-cli-29.5 — Bob Mac Capture close preview, footer, and notifications

[Bead Pages](../README.md) / [bob-cli-29](README.md) / bob-cli-29.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.2i](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.2i.md) · **Assignee:** `bob-cli-29.5` · **Size:** medium
**Created:** 2026-09-28 06:24:49 EDT · **Closed:** 2026-09-28 08:36:27 EDT
**Plan:** [202609/capture\_pomodoro\_close.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/capture_pomodoro_close.md)

## Description

mac-close-preview: in bob-mac-capture, decode the additive `pomodoro_close` contract. Render the dedicated close card (session, timing chip, task rows with transitions and Work Log previews, next session), including the variants for link and new-task closes. Add the Close footer and notifications, fix stale preview state, and add fake-bob fixtures generated from real bob output, tests, README updates, and green macOS CI.

## Notes

[2026-09-28T12:36:07Z · bob-cli-29.5] PROPOSED FOLLOW-UP: Run just format-lint, build, and test with Xcode 26 or macOS CI; this Linux workspace has no selected Apple developer tools.

[2026-09-28T12:36:27Z · bob-cli-29.5] Implemented close JSON decoding, preview cards for session/link/new-task closes, the Close footer, notifications, stale-preview clearing, README updates, and real-bob fixtures. Verified fixture JSON and fake-bob smoke output plus git diff --check. just format-lint and just test were blocked because no Apple developer tools are selected; proposed macOS verification follow-up is recorded.

## Dependencies

- **Depends on:** [bob-cli-29.3](bob-cli-29.3.md) ✓ · ⧖ 2026-09-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-29.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-29.5/README.md) | [bob-cli-29.5](bob-cli-29.5.md) | 0 |
