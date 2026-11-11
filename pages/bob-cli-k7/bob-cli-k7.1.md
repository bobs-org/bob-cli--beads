# Bead: bob-cli-k7.1 — Umbrella rule in the contract, memory, and Rust

[Bead Pages](../README.md) / [bob-cli-k7](README.md) / bob-cli-k7.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1b8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1b8.md) · **Assignee:** `bob-cli-k7.1` · **Size:** medium
**Created:** 2026-11-11 07:57:57 EST · **Closed:** 2026-11-11 08:43:30 EST
**Plan:** [202611/keep\_moving\_link\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/keep_moving_link_marks.md)

## Description

umbrella-rule: in bob-cli, redefine leaf projects as every recognised project except umbrellas (root projects whose ^prj carries a Sub-projects line); update §12.15–§12.17, projects/pomodoro-homes/json-outputs docs, the accepted memory decisions, and Rust is_leaf_project plus its LP/KM tests.

## Notes

[2026-11-11T13:20:40Z · bob-cli-k7.1] PROPOSED FOLLOW-UP: just docs-check fails identically on the clean base tree — reference pages capture-panel, capture-previews, keyboard, protocol, and bob-navigation-hotkeys exceed the 6000-word cap (already tracked by bob-cli-jz and bob-cli-h9)

[2026-11-11T13:43:30Z · bob-cli-k7.1--1] Verified umbrella-leaf rule in docs §12.15–§12.17, glossary:leaf-project, ProjectSurface.subprojects_listed, and is_leaf_project. LP1–LP17, KM6, and KM33 pass; sase tool run check 131fc1f7dd47e66b3ff2e3613b9f4544 succeeded (exit 0). No --epic-symbol leftovers. just docs-check still fails on the clean tree (bob-cli-jz, bob-cli-h9) and is recorded as follow-up.

## Dependencies

- **Blocks:** [bob-cli-k7.2](bob-cli-k7.2.md) ✓ · ⧖ 2026-11-11
- **Blocks:** [bob-cli-k7.3](bob-cli-k7.3.md) ✓ · ⧖ 2026-11-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-k7.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-k7.1.md) | [bob-cli-k7.1](bob-cli-k7.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b2c3697`](https://github.com/bobs-org/bob-cli/commit/b2c3697e8c57c5c2091b1df207d9bed3b38382f3) | feat(keep-moving): skip only umbrella projects, not every root | [bob-cli-k7.1](bob-cli-k7.1.md) | 2026-11-11 08:44:49 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-k7.1--1][1] | Need current bead status, notes, and remaining work after failed host completion | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-k7.1.md

<!-- sase:referenced-by:end -->
