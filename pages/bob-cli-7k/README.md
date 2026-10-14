# Bead: bob-cli-7k — Bob Refs ⌃Y Copy card

[Bead Pages](../README.md) / bob-cli-7k

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.19.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.19.linker.w0.md) · **Assignee:** `bob-cli-7k.land`
**Created:** 2026-10-14 09:32:30 EDT
**Plan:** [202610/refs\_ctrl\_y\_copy\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/refs_ctrl_y_copy_card.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/refs_ctrl_y_copy_card.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/refs_ctrl_y_copy_card.md

<!-- sase:links:end -->

## Description

In Bob Mac Capture's Refs panel, ⌃Y turns the inspector column into a Copy card where one keypress copies a precise handle for the selected reference (marker ID, title, wiki link, sources, paths, the PDF file, the reading task, research ref, or one or all of your notes). The copy is checked, Refs hides so the next ⌘V lands where you came from, and a glass HUD confirms what was copied. A highlight picker and ⌥ alternates follow.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-7k.1](bob-cli-7k.1.md) | bob-cli serializes the frontmatter id as marker\_id | ✓ closed | small | 2026-10-14 | 1 | 1 |
| [bob-cli-7k.2](bob-cli-7k.2.md) | RefsCore decoding, copy catalog, formats, key map, and card state machine | ✓ closed | medium | 2026-10-14 | 1 | 1 |
| [bob-cli-7k.3](bob-cli-7k.3.md) | App building blocks for the Copy card and HUD (not yet wired) | ✓ closed | medium | 2026-10-14 | 1 | 1 |
| [bob-cli-7k.4](bob-cli-7k.4.md) | Wire ⌃Y, the card lifecycle, hide-on-copy, ⌘K, footer, and README | ✓ closed | medium | 2026-10-14 | 1 | 1 |
| [bob-cli-7k.5](bob-cli-7k.5.md) | H highlight picker layer | ✓ closed | medium | 2026-10-14 | 1 | 1 |
| [bob-cli-7k.6](bob-cli-7k.6.md) | ⌥ alternates and the Obsidian link row | ✓ closed | medium | 2026-10-14 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-7k: Bob Refs ⌃Y Copy card [in_progress]"]
    n1["bob-cli-7k.1: bob-cli serializes the frontmatter id as marker_id [closed]"]
    n2["bob-cli-7k.2: RefsCore decoding, copy catalog, formats, key map, and card state machine [closed]"]
    n3["bob-cli-7k.3: App building blocks for the Copy card and HUD (not yet wired) [closed]"]
    n4["bob-cli-7k.4: Wire ⌃Y, the card lifecycle, hide-on-copy, ⌘K, footer, and README [closed]"]
    n5["bob-cli-7k.5: H highlight picker layer [closed]"]
    n6["bob-cli-7k.6: ⌥ alternates and the Obsidian link row [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n1 -.-> n4
    n2 -.-> n3
    n3 -.-> n4
    n4 -.-> n5
    n5 -.-> n6
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-7k.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-7k.1/README.md) | [bob-cli-7k.1](bob-cli-7k.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-7k.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-7k.2/README.md) | [bob-cli-7k.2](bob-cli-7k.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-7k.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-7k.3/README.md) | [bob-cli-7k.3](bob-cli-7k.3.md) | 1 |
| [bbugyi200.apollo.bob-cli-7k.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-7k.4.md) | [bob-cli-7k.4](bob-cli-7k.4.md) | 1 |
| [bbugyi200.apollo.bob-cli-7k.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-7k.5/README.md) | [bob-cli-7k.5](bob-cli-7k.5.md) | 1 |
| [bbugyi200.apollo.bob-cli-7k.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-7k.6.md) | [bob-cli-7k.6](bob-cli-7k.6.md) | 1 |
| [bbugyi200.apollo.bob-cli-7k.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-7k.land/README.md) | [bob-cli-7k](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e7e98d2`](https://github.com/bobs-org/bob-cli/commit/e7e98d2e49e6c9b034e864dbbc263ffa0dbabf48) | feat(ref): expose marker ids in JSON | [bob-cli-7k.1](bob-cli-7k.1.md) | 2026-10-14 09:39:35 EDT |
| bob-mac-capture | [`bob-mac-capture@060d77b`](https://github.com/bobs-org/bob-mac-capture/commit/060d77b41a79df7b529c9085f184b76928c0cbbb) | feat(refs-core): implement copy catalog and card state machine | [bob-cli-7k.2](bob-cli-7k.2.md) | 2026-10-14 09:50:04 EDT |
| bob-mac-capture | [`bob-mac-capture@7e7d8d6`](https://github.com/bobs-org/bob-mac-capture/commit/7e7d8d628446cda13fa2a903ef2570c5010aa5d1) | feat(refs): add Copy card view, glass HUD, and checked pasteboard | [bob-cli-7k.3](bob-cli-7k.3.md) | 2026-10-14 10:20:24 EDT |
| bob-mac-capture | [`bob-mac-capture@c4b1a25`](https://github.com/bobs-org/bob-mac-capture/commit/c4b1a257db3bdde636697d7f22aee6aab7285417) | feat(refs): wire copy card interactions and footer | [bob-cli-7k.4](bob-cli-7k.4.md) | 2026-10-14 11:02:14 EDT |
| bob-mac-capture | [`bob-mac-capture@9b70c62`](https://github.com/bobs-org/bob-mac-capture/commit/9b70c629cea5a8d138f768bbbf3e5a92ef5cd574) | feat(refs): add H highlight picker layer | [bob-cli-7k.5](bob-cli-7k.5.md) | 2026-10-14 11:24:01 EDT |
| bob-mac-capture | [`bob-mac-capture@2b7b330`](https://github.com/bobs-org/bob-mac-capture/commit/2b7b330e31ddd612a55365e563869891c282a71e) | feat(refs): add Option copy alternates and Obsidian links | [bob-cli-7k.6](bob-cli-7k.6.md) | 2026-10-14 12:53:23 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-7k.5][1] | Need the epic design and remaining phase context | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-7k.5/README.md

<!-- sase:referenced-by:end -->
