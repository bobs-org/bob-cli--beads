# Bead: bob-cli-32.3 — Bob Mac Capture previews Work Log bullets and their details

[Bead Pages](../README.md) / [bob-cli-32](README.md) / bob-cli-32.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0uj](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0uj.md) · **Assignee:** `bob-cli-32.3` · **Size:** medium
**Created:** 2026-09-30 21:31:28 EDT · **Closed:** 2026-09-30 23:10:45 EDT
**Plan:** [202609/close\_work\_log\_bullets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/close_work_log_bullets.md)

## Description

mac: decode `details` and `typed_work_log_details`, and show each typed entry's
details under it on the close card. Reword the pending notice (the escape is
gone), and teach the bullet form in the hint (`=x ⌃J 1 wrote the tests`).
Regenerate the real-bob fixtures for bullet drafts, update tests and the README,
and get macOS CI green.

## Notes

[2026-10-01T03:10:45Z · bob-cli-32.3] mac phase done: decoded details/typed_work_log_details with decodeIfPresent defaults, close card renders each typed entry's details under it (secondary callout, tail-truncated, uncapped), hint teaches =x CTRL-J 1 bullet form, pending notice escape-free. Regenerated 5 real-bob fixtures from bob-cli master, updated fake-bob branches, CaptureCore + PanelModel tests, README. Verified: 536 CaptureCoreTests green on Linux, macOS CI green (run 36808886241 success). bob-cli tree untouched.

## Dependencies

- **Depends on:** [bob-cli-32.1](bob-cli-32.1.md) ✓ · ⧖ 2026-09-30
- **Depends on:** [bob-cli-32.2](bob-cli-32.2.md) ✓ · ⧖ 2026-09-30
- **Blocks:** [bob-cli-32.4](bob-cli-32.4.md) ✓ · ⧖ 2026-09-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-32.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-32.3/README.md) | [bob-cli-32.3](bob-cli-32.3.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@1c85058`](https://github.com/bobs-org/bob-mac-capture/commit/1c85058c4f9d2bc7c562d0a5a7e6d111d39e5bf5) | feat(capture): preview Work Log bullets and their details on the close card | [bob-cli-32.3](bob-cli-32.3.md) | 2026-09-30 22:59:05 EDT |
| bob-mac-capture | [`bob-mac-capture@0ff0de9`](https://github.com/bobs-org/bob-mac-capture/commit/0ff0de999056040ab09297445b92a1faad25335b) | fix(capture): serve the trimmed bullet placeholder as a plain close in fake-bob | [bob-cli-32.3](bob-cli-32.3.md) | 2026-09-30 23:05:27 EDT |
