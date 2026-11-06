# Bead: bob-cli-hz.3 — Mac adopts the = opener and post-token flip

[Bead Pages](../README.md) / [bob-cli-hz](README.md) / bob-cli-hz.3

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.198](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.198.md) · **Assignee:** `bob-cli-hz.3` · **Size:** medium
**Created:** 2026-11-06 12:50:21 EST
**Plan:** [202611/relation\_equals\_alias\_and\_direction\_flips.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/relation_equals_alias_and_direction_flips.md)

## Description

mac-equals-opener: the Mac forwards `=` and token-glued `~` to Bob and replaces the dash arm with an equals opener arm that keeps the Space/Escape restores. It applies `toggle_relation_direction` natively without a picker and deletes every relation `-` path.

## Notes

[2026-11-06T22:01:22Z · bob-cli-hz.3--3] PROPOSED FOLLOW-UP: 12 pre-existing macOS CI failures on clean base cbb50dc (word motion, comma x2, backslash/slash aliases, period x2, semicolon, delayed alias, native undo, move undo) reproduce identically without phase changes; master runs 42278025697 and 42268256300 show same 12. Needs triage as CI/task bead.

## Dependencies

- **Depends on:** [bob-cli-hz.1](bob-cli-hz.1.md) ✓ · ⧖ 2026-11-06
- **Depends on:** [bob-cli-hz.2](bob-cli-hz.2.md) ✓ · ⧖ 2026-11-06
- **Blocks:** [bob-cli-hz.4](bob-cli-hz.4.md) ◐ · ⧖ 2026-11-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-hz.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hz.3.md) | [bob-cli-hz.3](bob-cli-hz.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@418604a`](https://github.com/bobs-org/bob-mac-capture/commit/418604a58a502ca6cadd8a7442eca0257901e66d) | feat(mac-capture)!: adopt = opener and post-token relation flips | [bob-cli-hz.3](bob-cli-hz.3.md) | 2026-11-06 17:04:07 EST |
