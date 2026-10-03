# Bead: bob-cli-3u.4 — Present the dependency picker and preview in Bob Mac Capture

[Bead Pages](../README.md) / [bob-cli-3u](README.md) / bob-cli-3u.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.4m](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.4m.md) · **Assignee:** `bob-cli-3u.4` · **Size:** medium
**Created:** 2026-10-03 09:11:57 EDT · **Closed:** 2026-10-03 11:48:06 EDT
**Plan:** [202610/capture\_task\_dependencies.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_task_dependencies.md)

## Description

dependency-mac: consume Bob's contract in a dependency picker, block-ID flow, semantic highlighting, and accessible task preview.

## Notes

[2026-10-03T15:47:57Z · bob-cli-3u.4] PROPOSED FOLLOW-UP: Run macOS-gated verification for commit 680e17f (just all, BOB_MAC_CAPTURE_RENDER_DIR PNG review at 760/620 light/dark+contrast, VoiceOver/focus pass, large-vault filter check) — Linux host has no Swift toolchain

[2026-10-03T15:48:06Z · bob-cli-3u.4] Implemented dependency picker+preview in bob-mac-capture commit 680e17f (pushed to origin master). Verified: real-bob JSON fixtures decode (query/owner/note_path/locator/guards/dependency_replacement/dependency_update), fake-bob branches pass locally (parse/complete/task-id), Swift test files added (index/decoding/client/panel/design/render states), bob-cli tree untouched, no epic-symbols. macOS build/tests/PNG review not runnable on this Linux host — recorded as follow-up for 3u.5/land.

## Dependencies

- **Depends on:** [bob-cli-3u.1](bob-cli-3u.1.md) ✓ · ⧖ 2026-10-03
- **Depends on:** [bob-cli-3u.2](bob-cli-3u.2.md) ✓ · ⧖ 2026-10-03
- **Depends on:** [bob-cli-3u.3](bob-cli-3u.3.md) ✓ · ⧖ 2026-10-03
- **Blocks:** [bob-cli-3u.5](bob-cli-3u.5.md) ✓ · ⧖ 2026-10-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-3u.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-3u.4/README.md) | [bob-cli-3u.4](bob-cli-3u.4.md) | 0 |
