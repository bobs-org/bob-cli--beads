# Bead: bob-cli-52.8 — Bob Mac Capture presents reference items

[Bead Pages](../README.md) / [bob-cli-52](README.md) / bob-cli-52.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.3w.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.3w.linker.w1.md) · **Assignee:** `bob-cli-52.8` · **Size:** medium
**Created:** 2026-10-07 08:11:17 EDT · **Closed:** 2026-10-07 11:28:48 EDT
**Plan:** [202610/url\_capture\_ref\_routing.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/url_capture_ref_routing.md)

## Description

mac: in the linked bob-mac-capture repo, tolerantly decode the `ref` object; add a reference card, status text, notification, and a link-colored `ref_url` span; open only targets that really exist; add `~/.local/bin` to PATH; and add fixtures recorded from real bob output, tests, README, and green macOS CI.

## Notes

[2026-10-07T15:28:48Z · bob-cli-52.8] mac phase done in bob-mac-capture: tolerant ref decode, CaptureRefPresentation card/status/notification, ref_url link span+underline, open-only-existing, ~/.local/bin PATH, 8 real-bob fixtures, CaptureCore (713 pass on Linux) + panel tests, README; macOS CI green on b19c913 (build+test+bundle+smoke+install)

## Dependencies

- **Depends on:** [bob-cli-52.7](bob-cli-52.7.md) ✓ · ⧖ 2026-10-07
- **Blocks:** [bob-cli-52.9](bob-cli-52.9.md) ✓ · ⧖ 2026-10-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-52.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-52.8/README.md) | [bob-cli-52.8](bob-cli-52.8.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@bf43ab2`](https://github.com/bobs-org/bob-mac-capture/commit/bf43ab24f3aeb47beb63cf7a64eb874e86013e78) | feat(capture): present reading-queue reference items | [bob-cli-52.8](bob-cli-52.8.md) | 2026-10-07 11:05:41 EDT |
| bob-mac-capture | [`bob-mac-capture@b19c913`](https://github.com/bobs-org/bob-mac-capture/commit/b19c91306bb84ebf12a6c63c4ac70d4de4f55a5c) | fix(capture): restore ViewBuilder on the completion card | [bob-cli-52.8](bob-cli-52.8.md) | 2026-10-07 11:09:21 EDT |
