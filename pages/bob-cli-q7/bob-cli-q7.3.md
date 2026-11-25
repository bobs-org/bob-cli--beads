# Bead: bob-cli-q7.3 — bob-plugins: any-line block fallback in the Go To re-find ladder

[Bead Pages](../README.md) / [bob-cli-q7](README.md) / bob-cli-q7.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1g6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1g6.md) · **Assignee:** `bob-cli-q7.3` · **Size:** small
**Created:** 2026-11-25 15:25:24 EST · **Closed:** 2026-11-25 15:35:52 EST
**Plan:** [202611/caret\_address\_goto\_capture.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/caret_address_goto_capture.md)

## Description

plugin-refind: let bob-goto-task re-find a unique non-task line carrying ^block when the task-only lookup misses, with tests, docs, build, and plugin sync.

## Notes

[2026-11-25T20:35:38Z · bob-cli-q7.3] PROPOSED FOLLOW-UP: npm run docs:check fails identically on the clean plugin tree — reference pages capture-syntax.md (6011), bob-ledger-tools.md (6002), and bob-navigation-hotkeys.md (6068) exceed the 6000-word cap; tracked by bob-cli-jz, bob-cli-il, and bob-cli-ob

[2026-11-25T20:35:52Z · bob-cli-q7.3] Verified plugin-refind: findAnyLineByBlockId re-finds a unique unfenced non-task ^block after the task-only lookup misses (heading/bullet, fenced IDs ignored, duplicates fall through to digest/clamp, task-first precedence unchanged). npm run build, npm test (9614 pass / 0 fail), and bob plugins sync deployed bob-navigation-hotkeys. npm run docs:check fails identically on the clean tree (word-cap pages tracked by bob-cli-jz, bob-cli-il, bob-cli-ob). No --epic-symbol leftovers.

## Dependencies

- **Blocks:** [bob-cli-q7.6](bob-cli-q7.6.md) ◐ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q7.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q7.3/README.md) | [bob-cli-q7.3](bob-cli-q7.3.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q7.3][1] | Need the phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q7.3/README.md

<!-- sase:referenced-by:end -->
