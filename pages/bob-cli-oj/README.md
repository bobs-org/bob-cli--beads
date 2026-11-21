# Bead: bob-cli-oj — \[N / \]N group jumps for days, periods, records, and any note

[Bead Pages](../README.md) / bob-cli-oj

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1es](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1es.md) · **Assignee:** `bob-cli-oj.land`
**Created:** 2026-11-21 07:41:34 EST
**Plan:** [202611/bracket\_n\_group\_jumps.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bracket_n_group_jumps.md)

## Description

`[N` / `]N` (and `[{` / `]}` after any `n` walk) open the first note of the previous / next group on every canonical daily, week, and quarter note, on records of albums that set `walk_by`, and on any note whose nav line carries `«` / `»` links. `[n` / `]n` walk a grouped album one group at a time. The property card's docked rail and the links walker footer show the same group stops, and a stop whose note does not exist yet looks clearly, calmly different from one that will never be created.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-oj.1](bob-cli-oj.1.md) | Group-link grammar, one resolver, and the \[N / \]N commands | ◐ in_progress | medium | 2026-11-21 | 1 | 0 |
| [bob-cli-oj.2](bob-cli-oj.2.md) | Calendar group provider, legacy step fill-in, and the pre-adoption guard | ✓ closed | medium | 2026-11-21 | 1 | 1 |
| [bob-cli-oj.3](bob-cli-oj.3.md) | Album \`walk\_by\` and group-major record walk lines in bob | ◐ in_progress | large | 2026-11-21 | 1 | 0 |
| [bob-cli-oj.4](bob-cli-oj.4.md) | Grouped record walk model and the record group provider | ◐ in_progress | medium | 2026-11-21 | 1 | 0 |
| [bob-cli-oj.5](bob-cli-oj.5.md) | The group row at the bottom of property cards | ◐ in_progress | large | 2026-11-21 | 1 | 0 |
| [bob-cli-oj.6](bob-cli-oj.6.md) | Group arms and hints in the links walker footer | ◐ in_progress | medium | 2026-11-21 | 1 | 0 |
| [bob-cli-oj.7](bob-cli-oj.7.md) | Album adoption, real-Obsidian proof, and final deploy | ◐ in_progress | medium | 2026-11-21 | 1 | 0 |
| [bob-cli-oj.8](bob-cli-oj.8.md) | Accepted memory updates | ◐ in_progress | small | 2026-11-21 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-oj: [N / ]N group jumps for days, periods, records, and any note [in_progress]"]
    n1["bob-cli-oj.1: Group-link grammar, one resolver, and the [N / ]N commands [in_progress]"]
    n2["bob-cli-oj.2: Calendar group provider, legacy step fill-in, and the pre-adoption guard [closed]"]
    n3["bob-cli-oj.3: Album `walk_by` and group-major record walk lines in bob [in_progress]"]
    n4["bob-cli-oj.3.1: Album walk_by and guarded grouped record walks [in_progress]"]
    n5["bob-cli-oj.3.1.1: Parse walk_by and publish one grouped walk model [in_progress]"]
    n6["bob-cli-oj.3.1.2: Apply grouped record moves in one guarded transaction [in_progress]"]
    n7["bob-cli-oj.3.1.3: Add reversible walk_by updates to the album writer [in_progress]"]
    n8["bob-cli-oj.3.1.4: Document and verify the complete grouped walk contract [in_progress]"]
    n9["bob-cli-oj.4: Grouped record walk model and the record group provider [in_progress]"]
    n10["bob-cli-oj.5: The group row at the bottom of property cards [in_progress]"]
    n11["bob-cli-oj.6: Group arms and hints in the links walker footer [in_progress]"]
    n12["bob-cli-oj.7: Album adoption, real-Obsidian proof, and final deploy [in_progress]"]
    n13["bob-cli-oj.8: Accepted memory updates [in_progress]"]
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
    n0 --> n11
    n0 --> n12
    n0 --> n13
    n1 -.-> n10
    n1 -.-> n11
    n2 -.-> n9
    n2 -.-> n10
    n2 -.-> n11
    n3 -.-> n9
    n5 -.-> n6
    n6 -.-> n7
    n7 -.-> n8
    n9 -.-> n10
    n9 -.-> n11
    n10 -.-> n12
    n11 -.-> n12
    n12 -.-> n13
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-oj.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.1/README.md) | [bob-cli-oj.1](bob-cli-oj.1.md) | 0 |
| [bbugyi200.athena.bob-cli-oj.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.2/README.md) | [bob-cli-oj.2](bob-cli-oj.2.md) | 1 |
| [bbugyi200.athena.bob-cli-oj.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-oj.3.md) | [bob-cli-oj.3](bob-cli-oj.3.md) | 0 |
| [bbugyi200.athena.bob-cli-oj.3.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.3.1.1/README.md) | [bob-cli-oj.3.1.1](bob-cli-oj.3.1.1.md) | 0 |
| [bbugyi200.athena.bob-cli-oj.3.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.3.1.2/README.md) | [bob-cli-oj.3.1.2](bob-cli-oj.3.1.2.md) | 0 |
| [bbugyi200.athena.bob-cli-oj.3.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.3.1.3/README.md) | [bob-cli-oj.3.1.3](bob-cli-oj.3.1.3.md) | 0 |
| [bbugyi200.athena.bob-cli-oj.3.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.3.1.4/README.md) | [bob-cli-oj.3.1.4](bob-cli-oj.3.1.4.md) | 0 |
| [bbugyi200.athena.bob-cli-oj.3.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.3.1.land/README.md) | [bob-cli-oj.3.1](bob-cli-oj.3.1.md) | 0 |
| [bbugyi200.athena.bob-cli-oj.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.4/README.md) | [bob-cli-oj.4](bob-cli-oj.4.md) | 0 |
| [bbugyi200.athena.bob-cli-oj.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5/README.md) | [bob-cli-oj.5](bob-cli-oj.5.md) | 0 |
| [bbugyi200.athena.bob-cli-oj.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.6/README.md) | [bob-cli-oj.6](bob-cli-oj.6.md) | 0 |
| [bbugyi200.athena.bob-cli-oj.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.7/README.md) | [bob-cli-oj.7](bob-cli-oj.7.md) | 0 |
| [bbugyi200.athena.bob-cli-oj.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.8/README.md) | [bob-cli-oj.8](bob-cli-oj.8.md) | 0 |
| [bbugyi200.athena.bob-cli-oj.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.land/README.md) | [bob-cli-oj](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@168b665`](https://github.com/bobs-org/bob-plugins/commit/168b665d35c36ec1f28309c6abca21219f161c39) | feat(ledger-tools): add api.navGroups v1 calendar group stops | [bob-cli-oj.2](bob-cli-oj.2.md) | 2026-11-21 08:06:42 EST |
