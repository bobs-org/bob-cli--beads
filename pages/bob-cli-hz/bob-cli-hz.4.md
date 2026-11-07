# Bead: bob-cli-hz.4 — Fast == escape in the editor and picker

[Bead Pages](../README.md) / [bob-cli-hz](README.md) / bob-cli-hz.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.198](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.198.md) · **Assignee:** `bob-cli-hz.4` · **Size:** medium
**Created:** 2026-11-06 12:50:21 EST · **Closed:** 2026-11-06 19:45:03 EST
**Plan:** [202611/relation\_equals\_alias\_and\_direction\_flips.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/relation_equals_alias_and_direction_flips.md)

## Description

equals-escape: one shared equals-gesture record with a ~350 ms key-to-key window, so a fast second `=` undoes whatever the first `=` did and types one `=`. Covers the editor before and after Bob replies, every flip, and the picker; the card reuses it.

## Notes

[2026-11-07T00:45:03Z · bob-cli-hz.4] Equals-escape implemented in bob-mac-capture (shared CaptureEqualsGestureArm record, fast-== undo in editor/picker/card, before-reply ==/=~ probe, opener subtitle, docs, 15 new tests). Verified: just portable-check green (2261 tests), just docs-check green, epic-symbols clean. macOS UNVERIFIED: typecheck-tests started twice on mac scratch /tmp/bob-mac-check-hz4 (reached [8/18]) but the mac went unreachable mid-build and stayed dark; focused suites never ran. Monitor m8sqx8 left polling to finish the mac typecheck when the mac wakes; land agent must confirm macOS CI green.

## Dependencies

- **Depends on:** [bob-cli-hz.3](bob-cli-hz.3.md) ✓ · ⧖ 2026-11-06
- **Blocks:** [bob-cli-hz.5](bob-cli-hz.5.md) ◐ · ⧖ 2026-11-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-hz.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hz.4.md) | [bob-cli-hz.4](bob-cli-hz.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@4fbbe84`](https://github.com/bobs-org/bob-mac-capture/commit/4fbbe84c5ffb4e8d6d0a6934410cfe5533e69e9c) | feat(mac-capture): fast == escape in the editor and picker | [bob-cli-hz.4](bob-cli-hz.4.md) | 2026-11-06 20:19:10 EST |
