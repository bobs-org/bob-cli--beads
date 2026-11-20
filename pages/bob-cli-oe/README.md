# Bead: bob-cli-oe — Ctrl+J jump pin on the successor card

[Bead Pages](../README.md) / bob-cli-oe

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5m.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5m.linker.w0.md) · **Assignee:** `bob-cli-oe.land`
**Created:** 2026-11-20 17:03:14 EST
**Plan:** [202611/successor\_jump\_pin.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/successor_jump_pin.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/successor_jump_pin.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/successor_jump_pin.md

<!-- sase:links:end -->

## Description

On the successor card in Obsidian and in Mac Capture, Ctrl+J pins one offer as the jump successor. The pinned offer can still be left open, pulled in, marked Done, or canceled. Once every write of the triggering close or capture has landed, Obsidian opens that task's note and focuses its line. The pin never writes to the vault, wins over the Cmd+Return open-notes landing, parks a ]s walk instead of advancing it, and never fails the close if the target can't be found.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-oe.1](bob-cli-oe.1.md) | bob capture --jump-offer and the jump JSON contract | ✓ closed | medium | 2026-11-20 | 1 | 1 |
| [bob-cli-oe.2](bob-cli-oe.2.md) | Obsidian successor card pin (picker API v5) | ✓ closed | medium | 2026-11-20 | 1 | 0 |
| [bob-cli-oe.3](bob-cli-oe.3.md) | Obsidian landing API, walk follow, and receipt line | ◐ in_progress | medium | 2026-11-20 | 1 | 0 |
| [bob-cli-oe.4](bob-cli-oe.4.md) | task-status-cycler honors the pin after every managed Done | ◐ in_progress | medium | 2026-11-20 | 1 | 0 |
| [bob-cli-oe.5](bob-cli-oe.5.md) | Wire the remaining Obsidian picker callers | ◐ in_progress | medium | 2026-11-20 | 1 | 0 |
| [bob-cli-oe.6](bob-cli-oe.6.md) | Mac Capture Pull-In card pin | ◐ in_progress | medium | 2026-11-20 | 1 | 0 |
| [bob-cli-oe.7](bob-cli-oe.7.md) | Walk docs, decision record, and glossary | ◐ in_progress | small | 2026-11-20 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-oe: Ctrl+J jump pin on the successor card [in_progress]"]
    n1["bob-cli-oe.1: bob capture --jump-offer and the jump JSON contract [closed]"]
    n2["bob-cli-oe.2: Obsidian successor card pin (picker API v5) [closed]"]
    n3["bob-cli-oe.3: Obsidian landing API, walk follow, and receipt line [in_progress]"]
    n4["bob-cli-oe.4: task-status-cycler honors the pin after every managed Done [in_progress]"]
    n5["bob-cli-oe.5: Wire the remaining Obsidian picker callers [in_progress]"]
    n6["bob-cli-oe.6: Mac Capture Pull-In card pin [in_progress]"]
    n7["bob-cli-oe.7: Walk docs, decision record, and glossary [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n0 --> n7
    n1 -.-> n6
    n2 -.-> n3
    n3 -.-> n4
    n4 -.-> n5
    n5 -.-> n7
    n6 -.-> n7
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-oe.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-oe.1/README.md) | [bob-cli-oe.1](bob-cli-oe.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-oe.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-oe.2/README.md) | [bob-cli-oe.2](bob-cli-oe.2.md) | 0 |
| [bbugyi200.apollo.bob-cli-oe.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-oe.3/README.md) | [bob-cli-oe.3](bob-cli-oe.3.md) | 0 |
| [bbugyi200.apollo.bob-cli-oe.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-oe.4/README.md) | [bob-cli-oe.4](bob-cli-oe.4.md) | 0 |
| [bbugyi200.apollo.bob-cli-oe.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-oe.5/README.md) | [bob-cli-oe.5](bob-cli-oe.5.md) | 0 |
| [bbugyi200.apollo.bob-cli-oe.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-oe.6/README.md) | [bob-cli-oe.6](bob-cli-oe.6.md) | 0 |
| [bbugyi200.apollo.bob-cli-oe.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-oe.7/README.md) | [bob-cli-oe.7](bob-cli-oe.7.md) | 0 |
| [bbugyi200.apollo.bob-cli-oe.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-oe.land/README.md) | [bob-cli-oe](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`853246f`](https://github.com/bobs-org/bob-cli/commit/853246f0ee582f4559767323c101dd2d2597cf91) | feat(capture): add successor jump offer contract | [bob-cli-oe.1](bob-cli-oe.1.md) | 2026-11-20 17:53:09 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-oe.2][1] | Need parent epic scope and plan context | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-oe.2/README.md

<!-- sase:referenced-by:end -->
