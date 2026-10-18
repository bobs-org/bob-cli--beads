# Bead: bob-cli-9j.5 — Mac: commit an override only after its warning was shown

[Bead Pages](../README.md) / [bob-cli-9j](README.md) / bob-cli-9j.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase · **↺ Reopened:** ↺1
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.91](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.91.md) · **Assignee:** `bob-cli-9j.5` · **Size:** small
**Created:** 2026-10-18 16:26:21 EDT · **Closed:** 2026-10-18 19:30:18 EDT
**Plan:** [202610/eq\_overrides\_running\_pomodoro.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/eq_overrides_running_pomodoro.md)

## Previously Closed

> ↺ Closed 2026-10-18T23:16:48Z · done
>
> (none)
>
> Reopened 2026-10-18T23:20:24Z by `sase bead open`

## Description

mac-guard: pass `--refuse-override` on every submit whose on-screen preview did not show an override, and turn the refusal into a calm re-preview so the second Return commits with the banner visible.

## Notes

[2026-10-18T23:16:00Z · bob-cli-9j.5] PROPOSED FOLLOW-UP: Consider adding a decisions-web record for `=` overriding a running Pomodoro behind a warning — epic decision selected decision_record=no, so this phase made no memory edit.

[2026-10-18T23:16:48Z · bob-cli-9j.5] Added freshness-checked preview gating for --refuse-override on all Mac Capture submits, made Bob's override refusal keep the draft open and refresh the warning preview, and updated invocation tests. git diff --check passed; portable-check was attempted but could not run because this host has no Swift toolchain and athena lacks this workspace checkout.

[2026-10-18T23:30:18Z · bob-cli-9j.5] Mac Capture now gates real submits with --refuse-override unless the on-screen preview matches this draft, analysis generation, and bob client and shows an override; a pomodoro_override_refused answer keeps the draft, re-previews, and asks for Return again. Older bob unexpected-argument failures for --refuse-override retry without the flag and cache that per executable identity. CaptureCore tests including the new fallback cases passed on athena via just portable-check (1381 tests, 0 failures); git diff --check passed. macOS BobMacCapture targets were not type-checked because the Mac SSH host timed out.

## Dependencies

- **Depends on:** [bob-cli-9j.4](bob-cli-9j.4.md) ✓ · ⧖ 2026-10-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-9j.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-9j.5/README.md) | [bob-cli-9j.5](bob-cli-9j.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@12219ef`](https://github.com/bobs-org/bob-mac-capture/commit/12219ef6ce4f0e3a21e1cb85f2c1efcfc36b9e13) | feat(capture): guard Mac submits until override warning is on screen | [bob-cli-9j.5](bob-cli-9j.5.md) | 2026-10-18 19:31:43 EDT |
