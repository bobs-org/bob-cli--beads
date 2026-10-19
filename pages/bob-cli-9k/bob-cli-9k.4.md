# Bead: bob-cli-9k.4 — Homes on capture-pomodoros, bob plan, and bob pomodoro

[Bead Pages](../README.md) / [bob-cli-9k](README.md) / bob-cli-9k.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.4t.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.4t.linker.w0.md) · **Assignee:** `bob-cli-9k.4` · **Size:** medium
**Created:** 2026-10-18 16:35:49 EDT · **Closed:** 2026-10-18 17:51:39 EDT
**Plan:** [202610/pomodoro\_homes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/pomodoro_homes.md)

## Description

live-surfaces: add an additive `homes` object to capture-pomodoros --tasks entries and to bob plan JSON entries, and dim chips to capture-pomodoros human output. Make `bob pomodoro` print the derived label for unnamed sessions. Update the chezmoi menu-bar spec and tests, the docs, and the mac pom glossary.

## Notes

[2026-10-18T21:51:39Z · bob-cli-9k.4] just check passed; capture-pomodoros --tasks -f json median 7.19ms / max 11.33ms on athena (schema 1, homes present); chezmoi hammerspoon 150/150; just install; goldens updated for additive homes; named pomodoro skips resolver; unnamed linked prints chip after range; no leftover --epic-symbol entries.

## Dependencies

- **Depends on:** [bob-cli-9k.1](bob-cli-9k.1.md) ✓ · ⧖ 2026-10-18
- **Blocks:** [bob-cli-9k.7](bob-cli-9k.7.md) ✓ · ⧖ 2026-10-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-9k.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9k.4/README.md) | [bob-cli-9k.4](bob-cli-9k.4.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`196af9b`](https://github.com/bobs-org/bob-cli/commit/196af9b38d9bac93e7055c599a7640e0f9eac95a) | feat(pomodoro-homes): expose derived homes on live CLI surfaces | [bob-cli-9k.4](bob-cli-9k.4.md) | 2026-10-18 17:52:36 EDT |
| chezmoi | [`chezmoi@6259f0b`](https://github.com/bbugyi200/dotfiles/commit/6259f0bfd261e255bb92acf61d196829c3c72fcf) | feat(hammerspoon): show derived home labels for unnamed pomodoros | [bob-cli-9k.4](bob-cli-9k.4.md) | 2026-10-18 17:53:35 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-9k.4][1] | Need the phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9k.4/README.md

<!-- sase:referenced-by:end -->
