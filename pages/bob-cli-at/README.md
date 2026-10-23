# Bead: bob-cli-at — Open PDFs stay in step with bob (Highlights saves first, then reloads in place)

[Bead Pages](../README.md) / bob-cli-at

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.56.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.56.linker.w0.md) · **Assignee:** `bob-cli-at.land`
**Created:** 2026-10-23 11:44:15 EDT
**Plan:** [202610/highlights\_coordinated\_marker\_writes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/highlights_coordinated_marker_writes.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/highlights_coordinated_marker_writes.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/highlights_coordinated_marker_writes.md

<!-- sase:links:end -->

## Description

When `bob ref scan` or `bob ref sync -w` on the Mac updates a ref PDF's page-1 marker, it never again strands an open Highlights document. bob writes through a bounded macOS file-coordination write (`NSFileCoordinator`, `.forMerging`). macOS has Highlights save your unsaved annotations first, bob re-checks the marker in the fresh bytes and writes, and Highlights reloads the same tab in place: no dialog, no keystroke, no tab change. Anything uncertain becomes a hold: nothing is written for that PDF, and the next scan retries. That covers you actively reading in Highlights, Highlights not answering, and the marker changing under bob. CLI and JSON always report what happened. Bob Mac Capture posts one quiet, grouped notification, only when a PDF that is open in Highlights was refreshed or Highlights needs you. The feature ships behind `highlights.coordinate_pdf_writes` and is enabled after a guided real-Highlights acceptance test.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-at.1](bob-cli-at.1.md) | macOS file-coordination primitive | ✓ closed | medium | 2026-10-23 | 1 | 1 |
| [bob-cli-at.2](bob-cli-at.2.md) | Coordination config, reading-activity probe, and budgets | ✓ closed | small | 2026-10-23 | 1 | 1 |
| [bob-cli-at.3](bob-cli-at.3.md) | Coordinated marker writes, holds, and human reporting | ✓ closed | medium | 2026-10-23 | 1 | 1 |
| [bob-cli-at.4](bob-cli-at.4.md) | Scan JSON fields, scan receipt, and the Darwin notification | ✓ closed | medium | 2026-10-23 | 1 | 1 |
| [bob-cli-at.5](bob-cli-at.5.md) | Bob Mac Capture core decoding and open-PDF presentation | ✓ closed | medium | 2026-10-23 | 1 | 1 |
| [bob-cli-at.6](bob-cli-at.6.md) | Bob Mac Capture receipt observer, notifications, and settings | ✓ closed | medium | 2026-10-23 | 1 | 1 |
| [bob-cli-at.7](bob-cli-at.7.md) | Acceptance kit, docs consolidation, decision record, and follow-ups | ◐ in_progress | medium | 2026-10-23 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-at: Open PDFs stay in step with bob (Highlights saves first, then reloads in place) [in_progress]"]
    n1["bob-cli-at.1: macOS file-coordination primitive [closed]"]
    n2["bob-cli-at.2: Coordination config, reading-activity probe, and budgets [closed]"]
    n3["bob-cli-at.3: Coordinated marker writes, holds, and human reporting [closed]"]
    n4["bob-cli-at.4: Scan JSON fields, scan receipt, and the Darwin notification [closed]"]
    n5["bob-cli-at.5: Bob Mac Capture core decoding and open-PDF presentation [closed]"]
    n6["bob-cli-at.6: Bob Mac Capture receipt observer, notifications, and settings [closed]"]
    n7["bob-cli-at.7: Acceptance kit, docs consolidation, decision record, and follow-ups [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n0 --> n7
    n1 -.-> n3
    n2 -.-> n3
    n3 -.-> n4
    n4 -.-> n5
    n4 -.-> n7
    n5 -.-> n6
    n6 -.-> n7
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-at.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-at.1.md) | [bob-cli-at.1](bob-cli-at.1.md) | 1 |
| [bbugyi200.athena.bob-cli-at.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-at.2.md) | [bob-cli-at.2](bob-cli-at.2.md) | 1 |
| [bbugyi200.athena.bob-cli-at.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-at.3/README.md) | [bob-cli-at.3](bob-cli-at.3.md) | 1 |
| [bbugyi200.athena.bob-cli-at.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-at.4/README.md) | [bob-cli-at.4](bob-cli-at.4.md) | 1 |
| [bbugyi200.athena.bob-cli-at.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-at.5.md) | [bob-cli-at.5](bob-cli-at.5.md) | 1 |
| [bbugyi200.athena.bob-cli-at.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-at.6/README.md) | [bob-cli-at.6](bob-cli-at.6.md) | 1 |
| [bbugyi200.athena.bob-cli-at.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-at.7/README.md) | [bob-cli-at.7](bob-cli-at.7.md) | 0 |
| [bbugyi200.athena.bob-cli-at.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-at.land/README.md) | [bob-cli-at](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`6480e7c`](https://github.com/bobs-org/bob-cli/commit/6480e7cc7c84d168559cad6b4d3ec9c5831af3d6) | feat(highlights-ref): stage PDF write policy and reading-activity probe | [bob-cli-at.2](bob-cli-at.2.md) | 2026-10-23 12:21:55 EDT |
| bob-cli | [`0aec807`](https://github.com/bobs-org/bob-cli/commit/0aec807c422c4a1d3d1be6ba5daa078473242071) | feat(native): add bounded macOS file coordination | [bob-cli-at.1](bob-cli-at.1.md) | 2026-10-23 12:44:36 EDT |
| bob-cli | [`cd4bc7a`](https://github.com/bobs-org/bob-cli/commit/cd4bc7a0cb23cb6d1eb13fc2c66da7d17d6a9eb7) | feat(highlights): coordinate PDF marker writes with holds and human reporting | [bob-cli-at.3](bob-cli-at.3.md) | 2026-10-23 13:49:27 EDT |
| bob-cli | [`faa9a75`](https://github.com/bobs-org/bob-cli/commit/faa9a7579d681a4ccbfe47c39155b183df1ec13a) | feat(highlights-ref): add scan JSON held fields, scan receipt, and Darwin notification | [bob-cli-at.4](bob-cli-at.4.md) | 2026-10-23 14:32:05 EDT |
| bob-mac-capture | [`bob-mac-capture@9fb67f3`](https://github.com/bobs-org/bob-mac-capture/commit/9fb67f324f7500a63a184add96b4b03f4254f74f) | feat(refs): decode scan receipts and present PDF updates | [bob-cli-at.5](bob-cli-at.5.md) | 2026-10-23 15:28:44 EDT |
| bob-mac-capture | [`bob-mac-capture@6dc2c12`](https://github.com/bobs-org/bob-mac-capture/commit/6dc2c126ea4c1c7de683c672c714f48828690171) | feat(refs): observe scan receipts and notify for open PDF updates | [bob-cli-at.6](bob-cli-at.6.md) | 2026-10-23 15:56:42 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-at.2--2][1] | Need epic DECISIONS and phase list to confirm this phase's remaining work | 1 |
| read-by | [agent:bob-cli-at.3][2] | Need parent epic decisions, phase list, and design context | 1 |
| read-by | [agent:bob-cli-at.4][3] | epic context for phase 4 | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-at.2.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-at.3/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-at.4/README.md

<!-- sase:referenced-by:end -->
