# Bead: bob-cli-oj — \[N / \]N group jumps for days, periods, records, and any note

[Bead Pages](../README.md) / bob-cli-oj

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1es](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1es.md) · **Assignee:** `bob-cli-oj.land`
**Created:** 2026-11-21 07:41:34 EST
**Plan:** [202611/bracket\_n\_group\_jumps.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bracket_n_group_jumps.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/bracket_n_group_jumps.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bracket_n_group_jumps.md

<!-- sase:links:end -->

## Description

`[N` / `]N` (and `[{` / `]}` after any `n` walk) open the first note of the previous / next group on every canonical daily, week, and quarter note, on records of albums that set `walk_by`, and on any note whose nav line carries `«` / `»` links. `[n` / `]n` walk a grouped album one group at a time. The property card's docked rail and the links walker footer show the same group stops, and a stop whose note does not exist yet looks clearly, calmly different from one that will never be created.

## Notes

[2026-11-21T15:22:38Z · bob-cli-oj.3.1.land] DISCOVERED ISSUE: Triaged proposal from bob-cli-oj.3.1.4 note #1. plugin-apis.md is 8165/8000 words at bob-plugins 4e0ff78. This is a develop-tier warning (lint.py), not a second fatal docs-check error. Independent count/history shows 7996 before 168b665, 8131 after your calendar-groups phase commit 168b665 (oj.2), then 8165 after 6debb63 (oe.8.3). The existing headroom task bob-cli-ob covers the broader remediation; the oj.2 increment is causally yours and should be considered in outer landing. This is outside the grouped-walk child epic.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-oj.1](bob-cli-oj.1.md) | Group-link grammar, one resolver, and the \[N / \]N commands | ✓ closed | medium | 2026-11-21 | 1 | 2 |
| [bob-cli-oj.2](bob-cli-oj.2.md) | Calendar group provider, legacy step fill-in, and the pre-adoption guard | ✓ closed | medium | 2026-11-21 | 1 | 1 |
| [bob-cli-oj.3](bob-cli-oj.3.md) | Album \`walk\_by\` and group-major record walk lines in bob | ✓ closed | large | 2026-11-21 | 1 | 0 |
| [bob-cli-oj.4](bob-cli-oj.4.md) | Grouped record walk model and the record group provider | ✓ closed | medium | 2026-11-21 | 1 | 2 |
| [bob-cli-oj.5](bob-cli-oj.5.md) | The group row at the bottom of property cards | ◐ in_progress | large | 2026-11-21 | 1 | 0 |
| [bob-cli-oj.6](bob-cli-oj.6.md) | Group arms and hints in the links walker footer | ✓ closed | medium | 2026-11-21 | 1 | 1 |
| [bob-cli-oj.7](bob-cli-oj.7.md) | Album adoption, real-Obsidian proof, and final deploy | ◐ in_progress | medium | 2026-11-21 | 1 | 0 |
| [bob-cli-oj.8](bob-cli-oj.8.md) | Accepted memory updates | ◐ in_progress | small | 2026-11-21 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-oj: [N / ]N group jumps for days, periods, records, and any note [in_progress]"]
    n1["bob-cli-oj.1: Group-link grammar, one resolver, and the [N / ]N commands [closed]"]
    n2["bob-cli-oj.2: Calendar group provider, legacy step fill-in, and the pre-adoption guard [closed]"]
    n3["bob-cli-oj.3: Album `walk_by` and group-major record walk lines in bob [closed]"]
    n4["bob-cli-oj.3.1: Album walk_by and guarded grouped record walks [closed]"]
    n5["bob-cli-oj.3.1.1: Parse walk_by and publish one grouped walk model [closed]"]
    n6["bob-cli-oj.3.1.2: Apply grouped record moves in one guarded transaction [closed]"]
    n7["bob-cli-oj.3.1.3: Add reversible walk_by updates to the album writer [closed]"]
    n8["bob-cli-oj.3.1.4: Document and verify the complete grouped walk contract [closed]"]
    n9["bob-cli-oj.4: Grouped record walk model and the record group provider [closed]"]
    n10["bob-cli-oj.5: The group row at the bottom of property cards [in_progress]"]
    n11["bob-cli-oj.5.1: The group row at the bottom of property cards [in_progress]"]
    n12["bob-cli-oj.5.1.1: Kit group-row builder, rail missing-target states, and their CSS [closed]"]
    n13["bob-cli-oj.5.1.2: Day, week, and quarter cards adopt the group row and the derived step row [closed]"]
    n14["bob-cli-oj.5.1.3: Grouped record walk rail and the album card's \"walks by\" pill [in_progress]"]
    n15["bob-cli-oj.5.1.4: Preview matrix, real-Obsidian e2e runs, and final deploy for the group rail [in_progress]"]
    n16["bob-cli-oj.6: Group arms and hints in the links walker footer [closed]"]
    n17["bob-cli-oj.7: Album adoption, real-Obsidian proof, and final deploy [in_progress]"]
    n18["bob-cli-oj.8: Accepted memory updates [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n3 --> n4
    n4 --> n5
    n4 --> n6
    n4 --> n7
    n4 --> n8
    n0 --> n9
    n0 --> n10
    n10 --> n11
    n11 --> n12
    n11 --> n13
    n11 --> n14
    n11 --> n15
    n0 --> n16
    n0 --> n17
    n0 --> n18
    n1 -.-> n10
    n1 -.-> n16
    n2 -.-> n9
    n2 -.-> n10
    n2 -.-> n16
    n3 -.-> n9
    n5 -.-> n6
    n6 -.-> n7
    n7 -.-> n8
    n9 -.-> n10
    n9 -.-> n16
    n10 -.-> n17
    n12 -.-> n13
    n12 -.-> n14
    n13 -.-> n15
    n14 -.-> n15
    n16 -.-> n17
    n17 -.-> n18
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-oj.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-oj.1.md) | [bob-cli-oj.1](bob-cli-oj.1.md) | 2 |
| [bbugyi200.athena.bob-cli-oj.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.2/README.md) | [bob-cli-oj.2](bob-cli-oj.2.md) | 1 |
| [bbugyi200.athena.bob-cli-oj.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-oj.3.md) | [bob-cli-oj.3](bob-cli-oj.3.md) | 0 |
| [bbugyi200.athena.bob-cli-oj.3.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.3.1.1/README.md) | [bob-cli-oj.3.1.1](bob-cli-oj.3.1.1.md) | 1 |
| [bbugyi200.athena.bob-cli-oj.3.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-oj.3.1.2.md) | [bob-cli-oj.3.1.2](bob-cli-oj.3.1.2.md) | 1 |
| [bbugyi200.athena.bob-cli-oj.3.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.3.1.3/README.md) | [bob-cli-oj.3.1.3](bob-cli-oj.3.1.3.md) | 1 |
| [bbugyi200.athena.bob-cli-oj.3.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.3.1.4/README.md) | [bob-cli-oj.3.1.4](bob-cli-oj.3.1.4.md) | 1 |
| [bbugyi200.athena.bob-cli-oj.3.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-oj.3.1.land.md) | [bob-cli-oj.3.1](bob-cli-oj.3.1.md) | 2 |
| [bbugyi200.athena.bob-cli-oj.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-oj.4.md) | [bob-cli-oj.4](bob-cli-oj.4.md) | 2 |
| [bbugyi200.athena.bob-cli-oj.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-oj.5.md) | [bob-cli-oj.5](bob-cli-oj.5.md) | 0 |
| [bbugyi200.athena.bob-cli-oj.5.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.1/README.md) | [bob-cli-oj.5.1.1](bob-cli-oj.5.1.1.md) | 1 |
| [bbugyi200.athena.bob-cli-oj.5.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.2/README.md) | [bob-cli-oj.5.1.2](bob-cli-oj.5.1.2.md) | 1 |
| [bbugyi200.athena.bob-cli-oj.5.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.3/README.md) | [bob-cli-oj.5.1.3](bob-cli-oj.5.1.3.md) | 0 |
| [bbugyi200.athena.bob-cli-oj.5.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.4/README.md) | [bob-cli-oj.5.1.4](bob-cli-oj.5.1.4.md) | 0 |
| [bbugyi200.athena.bob-cli-oj.5.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.land/README.md) | [bob-cli-oj.5.1](bob-cli-oj.5.1.md) | 0 |
| [bbugyi200.athena.bob-cli-oj.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.6/README.md) | [bob-cli-oj.6](bob-cli-oj.6.md) | 1 |
| [bbugyi200.athena.bob-cli-oj.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.7/README.md) | [bob-cli-oj.7](bob-cli-oj.7.md) | 0 |
| [bbugyi200.athena.bob-cli-oj.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.8/README.md) | [bob-cli-oj.8](bob-cli-oj.8.md) | 0 |
| [bbugyi200.athena.bob-cli-oj.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.land/README.md) | [bob-cli-oj](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@168b665`](https://github.com/bobs-org/bob-plugins/commit/168b665d35c36ec1f28309c6abca21219f161c39) | feat(ledger-tools): add api.navGroups v1 calendar group stops | [bob-cli-oj.2](bob-cli-oj.2.md) | 2026-11-21 08:06:42 EST |
| bob-cli | [`e11f2a0`](https://github.com/bobs-org/bob-cli/commit/e11f2a0c5e9fa1cb0aefe01a4ccb1ca1785e0af1) | feat(albums): group record walks by declared walk\_by | [bob-cli-oj.3.1.1](bob-cli-oj.3.1.1.md) | 2026-11-21 08:25:36 EST |
| bob-cli | [`ce0dcc5`](https://github.com/bobs-org/bob-cli/commit/ce0dcc54cec50104991b4ad943de0566e7eba2b6) | feat(records): apply grouped walk updates | [bob-cli-oj.3.1.2](bob-cli-oj.3.1.2.md) | 2026-11-21 08:58:17 EST |
| bob-plugins | [`bob-plugins@51cf930`](https://github.com/bobs-org/bob-plugins/commit/51cf930da624ffaa5f0c950464ad55db1556e77a) | feat(navigation): restore group-link commands and guarded repeats | [bob-cli-oj.1](bob-cli-oj.1.md) | 2026-11-21 09:33:34 EST |
| bob-plugins | [`bob-plugins@983076e`](https://github.com/bobs-org/bob-plugins/commit/983076e6882c744f36e6fa513e9c2853bd160c36) | feat(navigation): land group-link resolver and guarded group jumps | [bob-cli-oj.1](bob-cli-oj.1.md) | 2026-11-21 09:42:42 EST |
| bob-cli | [`66866ea`](https://github.com/bobs-org/bob-cli/commit/66866ea114d6b8eded72d27d66169722d50c6920) | feat(albums): add reversible walk\_by updates to the album writer | [bob-cli-oj.3.1.3](bob-cli-oj.3.1.3.md) | 2026-11-21 09:48:58 EST |
| bob-cli | [`020ad4e`](https://github.com/bobs-org/bob-cli/commit/020ad4e6207f81fd9c633db21c48e1b8efdf3bba) | docs(albums): document grouped record walks | [bob-cli-oj.3.1.4](bob-cli-oj.3.1.4.md) | 2026-11-21 10:15:34 EST |
| bob-cli | [`7ac4fee`](https://github.com/bobs-org/bob-cli/commit/7ac4feeb043503a050e253dfe499da32c9ac1e04) | fix(albums): restore walk\_by at original slot and bind emitted selection | [bob-cli-oj.3.1](bob-cli-oj.3.1.md) | 2026-11-21 11:15:03 EST |
| bob-cli--plans | [`bob-cli--plans@761b2b8`](https://github.com/bobs-org/bob-cli--plans/commit/761b2b8b536aef795ef576ab2a98fb7f7256a9b3) | chore(plans): mark album\_walk\_by epic and landing repairs done | [bob-cli-oj.3.1](bob-cli-oj.3.1.md) | 2026-11-21 11:15:49 EST |
| bob-plugins | [`bob-plugins@d8dc11e`](https://github.com/bobs-org/bob-plugins/commit/d8dc11eafae367bf05b464be86ed4d1a10cfe05b) | feat(ledger-tools): add grouped record navigation | [bob-cli-oj.4](bob-cli-oj.4.md) | 2026-11-21 11:42:38 EST |
| bob-plugins | [`bob-plugins@bd8f2d4`](https://github.com/bobs-org/bob-plugins/commit/bd8f2d46219b794996e8563e3410bbc6e7e58e3c) | docs(plugins): refresh ledger tools inventory for 1.149.2 | [bob-cli-oj.4](bob-cli-oj.4.md) | 2026-11-21 11:56:43 EST |
| bob-plugins | [`bob-plugins@7b44b29`](https://github.com/bobs-org/bob-plugins/commit/7b44b29dc2b29584c2a7dcf0453309bc0a4f8821) | feat(ledger-tools): paint group arms and hints in the links walker footer | [bob-cli-oj.6](bob-cli-oj.6.md) | 2026-11-21 12:39:49 EST |
| bob-plugins | [`bob-plugins@c4953d3`](https://github.com/bobs-org/bob-plugins/commit/c4953d3d47b82dd5d615e9990d9471b3c4c49773) | feat(ledger-tools): add the property-card group row and missing-target states | [bob-cli-oj.5.1.1](bob-cli-oj.5.1.1.md) | 2026-11-21 12:48:44 EST |
| bob-plugins | [`bob-plugins@63e2f64`](https://github.com/bobs-org/bob-plugins/commit/63e2f6418a4f6135b59884ed888b67ccd9c14d68) | feat(ledger-tools): day, week, and quarter cards adopt the group row | [bob-cli-oj.5.1.2](bob-cli-oj.5.1.2.md) | 2026-11-21 13:15:37 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-oj.2][1] | Need parent epic DECISIONS, notes, and overall scope | 1 |
| read-by | [agent:bob-cli-oj.6][2] | Need sibling phase statuses so I do not redo landed work or collide with group-rail | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.6/README.md

<!-- sase:referenced-by:end -->
