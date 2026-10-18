# Bead: bob-cli-8x — Ctrl+Shift+Alt+B opens the Blocks… stage, Ctrl+Shift+B in reverse

[Bead Pages](../README.md) / bob-cli-8x

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.117](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.117.md) · **Assignee:** `bob-cli-8x.land`
**Created:** 2026-10-17 17:11:59 EDT
**Plan:** [202610/ctrl\_shift\_alt\_b\_blocks\_stage.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ctrl_shift_alt_b_blocks_stage.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/ctrl_shift_alt_b_blocks_stage.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ctrl_shift_alt_b_blocks_stage.md

<!-- sase:links:end -->

## Description

In Obsidian, Ctrl+Shift+Alt+B on task N (Task Card ⇧B) opens a Blocks… stage where Bryan picks the open tasks T that N blocks. Applying it writes N onto each T's Depends-On line. The bytes are exactly what Ctrl+Shift+B on T adding N would write: T becomes Blocked, its live links in today's Pomodoros are consumed, N takes over its lane, and N's BLOCKS mirror is updated. The stage previews every consequence before ↵, and BLOCKS chips gain ＋ / ×.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-8x.1](bob-cli-8x.1.md) | Blocks stage contract and RB vectors in the bob-cli docs | ✓ closed | medium | 2026-10-17 | 1 | 1 |
| [bob-cli-8x.2](bob-cli-8x.2.md) | Reverse dependency writer with forward-parity tests | ✓ closed | medium | 2026-10-17 | 1 | 1 |
| [bob-cli-8x.3](bob-cli-8x.3.md) | The Blocks… stage modal | ✓ closed | medium | 2026-10-17 | 1 | 1 |
| [bob-cli-8x.4](bob-cli-8x.4.md) | Task Card ⇧B row, Ctrl+Shift+Alt+B, and every other entry point | ✓ closed | medium | 2026-10-17 | 1 | 1 |
| [bob-cli-8x.5](bob-cli-8x.5.md) | BLOCKS chip ＋ / × through api.blocks | ✓ closed | small | 2026-10-17 | 1 | 1 |
| [bob-cli-8x.6](bob-cli-8x.6.md) | README, manifests, glossary, and the final sweep | ✓ closed | small | 2026-10-17 | 1 | 2 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-8x: Ctrl+Shift+Alt+B opens the Blocks… stage, Ctrl+Shift+B in reverse [in_progress]"]
    n1["bob-cli-8x.1: Blocks stage contract and RB vectors in the bob-cli docs [closed]"]
    n2["bob-cli-8x.2: Reverse dependency writer with forward-parity tests [closed]"]
    n3["bob-cli-8x.3: The Blocks… stage modal [closed]"]
    n4["bob-cli-8x.4: Task Card ⇧B row, Ctrl+Shift+Alt+B, and every other entry point [closed]"]
    n5["bob-cli-8x.5: BLOCKS chip ＋ / × through api.blocks [closed]"]
    n6["bob-cli-8x.6: README, manifests, glossary, and the final sweep [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n1 -.-> n2
    n2 -.-> n3
    n3 -.-> n4
    n4 -.-> n5
    n4 -.-> n6
    n5 -.-> n6
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-8x.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-8x.1/README.md) | [bob-cli-8x.1](bob-cli-8x.1.md) | 1 |
| [bbugyi200.athena.bob-cli-8x.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-8x.2/README.md) | [bob-cli-8x.2](bob-cli-8x.2.md) | 1 |
| [bbugyi200.athena.bob-cli-8x.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-8x.3/README.md) | [bob-cli-8x.3](bob-cli-8x.3.md) | 1 |
| [bbugyi200.athena.bob-cli-8x.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-8x.4/README.md) | [bob-cli-8x.4](bob-cli-8x.4.md) | 1 |
| [bbugyi200.athena.bob-cli-8x.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-8x.5/README.md) | [bob-cli-8x.5](bob-cli-8x.5.md) | 1 |
| [bbugyi200.athena.bob-cli-8x.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-8x.6/README.md) | [bob-cli-8x.6](bob-cli-8x.6.md) | 2 |
| [bbugyi200.athena.bob-cli-8x.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-8x.land/README.md) | [bob-cli-8x](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`30bdfb8`](https://github.com/bobs-org/bob-cli/commit/30bdfb8900be9cc7a24dc534e73f9e0712a2b5c7) | docs(task-dependencies): document reverse Blocks stage contract | [bob-cli-8x.1](bob-cli-8x.1.md) | 2026-10-17 17:26:11 EDT |
| bob-plugins | [`bob-plugins@8ca6a65`](https://github.com/bobs-org/bob-plugins/commit/8ca6a65eeca6b6f34403ae2e9840896e42a8cf1a) | feat(nav): add reverse Blocks writer with forward-parity tests | [bob-cli-8x.2](bob-cli-8x.2.md) | 2026-10-17 18:22:11 EDT |
| bob-plugins | [`bob-plugins@e3f3329`](https://github.com/bobs-org/bob-plugins/commit/e3f3329d9843cb6dbc2200652cf24754191720ca) | feat(nav): add reverse Blocks stage modal | [bob-cli-8x.3](bob-cli-8x.3.md) | 2026-10-17 19:04:26 EDT |
| bob-plugins | [`bob-plugins@10d12f4`](https://github.com/bobs-org/bob-plugins/commit/10d12f42aeb3944fe0ed54fa7c3c3da5c501486c) | feat(navigation): add Task Card Blocks entry points | [bob-cli-8x.4](bob-cli-8x.4.md) | 2026-10-17 19:28:45 EDT |
| bob-plugins | [`bob-plugins@254b32b`](https://github.com/bobs-org/bob-plugins/commit/254b32ba0ee7e54fc0a922de9fbf501701ae9540) | feat(ledger-tools): add BLOCKS chip ＋ / × through api.blocks | [bob-cli-8x.5](bob-cli-8x.5.md) | 2026-10-17 19:54:07 EDT |
| bob-cli | [`3ec4d0d`](https://github.com/bobs-org/bob-cli/commit/3ec4d0d232dbb178e01d0b4fe0761a66323f547f) | docs(dependencies): clarify editing from both ends | [bob-cli-8x.6](bob-cli-8x.6.md) | 2026-10-17 20:08:44 EDT |
| bob-plugins | [`bob-plugins@96a42c5`](https://github.com/bobs-org/bob-plugins/commit/96a42c56e9d338c0fd013cce4c1187bcba8b2b04) | docs(plugins): publish reverse Blocks stage gestures | [bob-cli-8x.6](bob-cli-8x.6.md) | 2026-10-17 20:09:51 EDT |
