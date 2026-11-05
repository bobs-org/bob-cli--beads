# Bead: bob-cli-h4.4 — Mac transfer card, status line, offers, notifications, and VoiceOver

[Bead Pages](../README.md) / [bob-cli-h4](README.md) / bob-cli-h4.4

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.188](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.188.md) · **Assignee:** `bob-cli-h4.4` · **Size:** medium
**Created:** 2026-11-04 14:57:19 EST
**Plan:** [202611/transfer\_previews.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/transfer_previews.md)

## Description

mac-transfer-card: replace the monospace transfer bands and the wire-word standard header with one designed transfer card that mirrors the draft. The card shows the verb, the source rows, an `↓ into` connector, the destination, consequence rows, the TODAY badge, and the offer rows. Also rewrite the status line, notification copy, and VoiceOver summary, regenerate rich recorded fixtures, and add design renders and docs.

## Notes

[2026-11-04T23:58:40Z · bob-cli-h4.4--5] Mac verification remains pending. The 45-minute retry failed before compilation because the remote shell received the literal $scratch path and could not cd into it. Tailscale currently reports the Mac offline, last seen 17 minutes ago; the rsynced scratch copy could not be checked or removed while offline. Earlier just portable-check (2,123 tests, 0 failures, 1 skipped), just docs-check, and 10 focused transfer presentation tests passed. Do not close until the Mac scratch bundle and just typecheck-tests are verified.

## Dependencies

- **Depends on:** [bob-cli-h4.2](bob-cli-h4.2.md) ✓ · ⧖ 2026-11-04
- **Blocks:** [bob-cli-h4.5](bob-cli-h4.5.md) ◐ · ⧖ 2026-11-04

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-h4.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-h4.4.md) | [bob-cli-h4.4](bob-cli-h4.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@e9dc5bd`](https://github.com/bobs-org/bob-mac-capture/commit/e9dc5bd91253cf0ad09671eb8c724cb5a37453a5) | feat(capture): render transfer previews as cards | [bob-cli-h4.4](bob-cli-h4.4.md) | 2026-11-04 19:42:16 EST |
