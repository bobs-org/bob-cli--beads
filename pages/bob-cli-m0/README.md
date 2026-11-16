# Bead: bob-cli-m0 — Ctrl+W window prefix for Obsidian vertical splits

[Bead Pages](../README.md) / bob-cli-m0

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.e9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.e9.md) · **Assignee:** `bob-cli-m0.land`
**Created:** 2026-11-15 20:01:48 EST
**Plan:** [202611/obsidian\_ctrl\_w\_window\_prefix.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/obsidian_ctrl_w_window_prefix.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/obsidian_ctrl_w_window_prefix.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/obsidian_ctrl_w_window_prefix.md

<!-- sase:links:end -->

## Description

In Bob's Obsidian, Ctrl+W followed by a key focuses, moves, and creates main-area splits from the keyboard. h/l focus the neighbouring split, H/L move the current tab into, out of, or across splits (creating and collapsing splits as needed) without losing its editor state, and a calm, theme-native hint shows exactly what each key will do.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-m0.1](bob-cli-m0.1.md) | Real-Obsidian layout and keyboard spike | ✓ closed | medium | 2026-11-15 | 1 | 1 |
| [bob-cli-m0.2](bob-cli-m0.2.md) | Pure layout model, planners, key table, and view model | ✓ closed | medium | 2026-11-15 | 1 | 0 |
| [bob-cli-m0.3](bob-cli-m0.3.md) | Live layout adapter and lossless executor | ✓ closed | medium | 2026-11-15 | 1 | 1 |
| [bob-cli-m0.4](bob-cli-m0.4.md) | Ring, card, minimap, and motion painter | ✓ closed | medium | 2026-11-15 | 1 | 1 |
| [bob-cli-m0.5](bob-cli-m0.5.md) | Ctrl+W prefix state machine | ✓ closed | medium | 2026-11-15 | 1 | 1 |
| [bob-cli-m0.6](bob-cli-m0.6.md) | Commands, focused-split underline, docs, acceptance, rollout | ✓ closed | medium | 2026-11-15 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-m0: Ctrl+W window prefix for Obsidian vertical splits [in_progress]"]
    n1["bob-cli-m0.1: Real-Obsidian layout and keyboard spike [closed]"]
    n2["bob-cli-m0.2: Pure layout model, planners, key table, and view model [closed]"]
    n3["bob-cli-m0.3: Live layout adapter and lossless executor [closed]"]
    n4["bob-cli-m0.4: Ring, card, minimap, and motion painter [closed]"]
    n5["bob-cli-m0.5: Ctrl+W prefix state machine [closed]"]
    n6["bob-cli-m0.6: Commands, focused-split underline, docs, acceptance, rollout [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n1 -.-> n3
    n2 -.-> n3
    n2 -.-> n4
    n3 -.-> n5
    n4 -.-> n5
    n5 -.-> n6
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-m0.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-m0.1/README.md) | [bob-cli-m0.1](bob-cli-m0.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-m0.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-m0.2.md) | [bob-cli-m0.2](bob-cli-m0.2.md) | 0 |
| [bbugyi200.apollo.bob-cli-m0.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-m0.3/README.md) | [bob-cli-m0.3](bob-cli-m0.3.md) | 1 |
| [bbugyi200.apollo.bob-cli-m0.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-m0.4.md) | [bob-cli-m0.4](bob-cli-m0.4.md) | 1 |
| [bbugyi200.apollo.bob-cli-m0.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-m0.5/README.md) | [bob-cli-m0.5](bob-cli-m0.5.md) | 1 |
| [bbugyi200.apollo.bob-cli-m0.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-m0.6/README.md) | [bob-cli-m0.6](bob-cli-m0.6.md) | 1 |
| [bbugyi200.apollo.bob-cli-m0.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-m0.land/README.md) | [bob-cli-m0](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@a2550d6`](https://github.com/bobs-org/bob-plugins/commit/a2550d69ef0cf0606dd4bd3647c7a43646d9e7f2) | feat(nav): add Ctrl+W window-prefix real-Obsidian spike e2e harness | [bob-cli-m0.1](bob-cli-m0.1.md) | 2026-11-15 21:05:21 EST |
| bob-plugins | [`bob-plugins@4678586`](https://github.com/bobs-org/bob-plugins/commit/4678586a48a18379888946803fd456361731c132) | feat(navigation-hotkeys): add lossless window prefix adapter | [bob-cli-m0.3](bob-cli-m0.3.md) | 2026-11-16 07:07:01 EST |
| bob-plugins | [`bob-plugins@1a9e304`](https://github.com/bobs-org/bob-plugins/commit/1a9e304d828b36c5735fcb42ccf14a43e894e8ea) | feat(navigation): paint Ctrl+W window-prefix hint | [bob-cli-m0.4](bob-cli-m0.4.md) | 2026-11-16 07:20:22 EST |
| bob-plugins | [`bob-plugins@c725370`](https://github.com/bobs-org/bob-plugins/commit/c72537068ac0601f42069cd8af3f53d928614ba8) | feat(navigation): add Ctrl+W prefix state machine | [bob-cli-m0.5](bob-cli-m0.5.md) | 2026-11-16 08:25:23 EST |
| bob-plugins | [`bob-plugins@0e16e30`](https://github.com/bobs-org/bob-plugins/commit/0e16e304142f94c70c78357f7bdfe4ded19d0db5) | feat(navigation): add Ctrl+W palette commands, focused-split underline, window-keys docs, and visual acceptance | [bob-cli-m0.6](bob-cli-m0.6.md) | 2026-11-16 09:12:12 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-m0.1][1] | epic scope | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-m0.1/README.md

<!-- sase:referenced-by:end -->
