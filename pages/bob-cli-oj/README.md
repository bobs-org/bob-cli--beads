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

_Plus 4 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bracket_n_group_jumps.md

<!-- sase:links:end -->

## Description

`[N` / `]N` (and `[{` / `]}` after any `n` walk) open the first note of the previous / next group on every canonical daily, week, and quarter note, on records of albums that set `walk_by`, and on any note whose nav line carries `«` / `»` links. `[n` / `]n` walk a grouped album one group at a time. The property card's docked rail and the links walker footer show the same group stops, and a stop whose note does not exist yet looks clearly, calmly different from one that will never be created.

## Notes

[2026-11-21T15:22:38Z · bob-cli-oj.3.1.land] DISCOVERED ISSUE: Triaged proposal from bob-cli-oj.3.1.4 note #1. plugin-apis.md is 8165/8000 words at bob-plugins 4e0ff78. This is a develop-tier warning (lint.py), not a second fatal docs-check error. Independent count/history shows 7996 before 168b665, 8131 after your calendar-groups phase commit 168b665 (oj.2), then 8165 after 6debb63 (oe.8.3). The existing headroom task bob-cli-ob covers the broader remediation; the oj.2 increment is causally yours and should be considered in outer landing. This is outside the grouped-walk child epic.

[2026-11-21T20:27:18Z · bryanbugyi34@gmail.com] The new bar that we added does not look great. Namely, the '<<' and '>>' don't look great and are not intuitive and the bottom bar is way to cluttered. See the 🔒 20261121\_152522.png screenshot for an example of what this looks like now. The epic lander agent should try to improve the situation before landing the epic.

[2026-11-21T22:10:03Z · bob-cli-oj.5.1.land] FOR THE bob-cli-oj LAND AGENT (from bob-cli-oj.5.1.land): Bryan's note #2 (the «/» arms looked bad and the bottom bar was cluttered) is addressed in Ledger Tools 1.157.0. It is the landing stitch for bob-cli-oj.5.1, committed by the host finalizer on top of bob-plugins ae305a3, and deployed with bob plugins sync.
Decisions taken (auto, final): layout = slim (the group row stays its own slim second row), glyph = skip (Lucide skip-back / skip-forward inline SVG), footer = yes.
Surfaces changed:
1. Property-card group row on day, week, and quarter cards and the grouped record walk rail. Arms show the skip mark and the group name only, with no «/» and no visible landing; the tooltip and accessible name carry the landing. The centre is just the tick track (title and hidden label carry `Day 6 of 7 in week W47` or `Section 2 of 4: … · 2 of 3`). A one-member group shows no centre or track, which is the screenshot case. Creatable and ghost arms use dashed or dotted underlines, not boxes; rail items and chips keep their boxes.
2. Status-bar links walker footer: the same mark (shared kit builder), no «/» in arm text, no `1/1` context, and `]n enters X` moves to the tooltip while the next group arm already names X.
Authored «/»/<< >> nav-line grammar and the conflict message are unchanged; Navigation Hotkeys is untouched.
bob-cli-oj.5.1 and phase bob-cli-oj.5 are closed (evidence in their close notes).
Left for you:
- the decisions-web follow-up (bob-cli-oj.5 note #1)
- bob-cli-oj.6 note #3, the walker-footer e2e geometryStable failure. I reproduced it identically on clean origin/master fc806cf: .bob-bracket-mode x = 819/956/1085/968 for s/w/n/b, width and height stable. So it predates this landing; no task was filed, to avoid duplicating that proposal.

[2026-11-22T00:16:09Z · bob-cli-o6.land] DISCOVERED ISSUE (routed by the bob-cli-o6 land agent): task bob-cli-ot (intention-card e2e yaml-done-returns timeout; yaml-invalid-stays-recoverable refusal notice missing) is caused by this epic's phase bob-cli-oj.6 commit 7b44b29 'paint group arms and hints in the links walker footer'. Attribution is decisive, not inferred: with the same debug bob and harness, the full intention-card e2e passes 82/82 at 9a15d52 (= 7b44b29~1) and yaml-done-returns fails at 7b44b29 (artifacts file:explicit:8290d9715c1214421e92b848 and file:explicit:a9a0d0dd3ca2361e423565a4, attached to bob-cli-ot with code pointers). The related-link suspicion on bob-cli-o6 ('Done-control return path may have regressed in o6.5') is cleared: all o6 commits are in the passing tree. Per task-bead rules this epic-caused issue is bob-cli-oj land-agent work before close; bob-cli-ot stays as the tracking task.

## Attachments

- 🔒 20261121\_152522.png · image/png · 2858×1728 · 983.287 KiB (private attachment)

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-oj.1](bob-cli-oj.1.md) | Group-link grammar, one resolver, and the \[N / \]N commands | ✓ closed | medium | 2026-11-21 | 1 | 0 |
| [bob-cli-oj.2](bob-cli-oj.2.md) | Calendar group provider, legacy step fill-in, and the pre-adoption guard | ✓ closed | medium | 2026-11-21 | 1 | 0 |
| [bob-cli-oj.3](bob-cli-oj.3.md) | Album \`walk\_by\` and group-major record walk lines in bob | ✓ closed | large | 2026-11-21 | 1 | 0 |
| [bob-cli-oj.4](bob-cli-oj.4.md) | Grouped record walk model and the record group provider | ✓ closed | medium | 2026-11-21 | 1 | 0 |
| [bob-cli-oj.5](bob-cli-oj.5.md) | The group row at the bottom of property cards | ✓ closed | large | 2026-11-21 | 1 | 0 |
| [bob-cli-oj.6](bob-cli-oj.6.md) | Group arms and hints in the links walker footer | ✓ closed | medium | 2026-11-21 | 1 | 0 |
| [bob-cli-oj.7](bob-cli-oj.7.md) | Album adoption, real-Obsidian proof, and final deploy | ✓ closed | medium | 2026-11-21 | 1 | 0 |
| [bob-cli-oj.8](bob-cli-oj.8.md) | Accepted memory updates | ◐ in_progress | small | 2026-11-21 | 1 | 1 |

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
    n10["bob-cli-oj.5: The group row at the bottom of property cards [closed]"]
    n11["bob-cli-oj.5.1: The group row at the bottom of property cards [closed]"]
    n12["bob-cli-oj.5.1.1: Kit group-row builder, rail missing-target states, and their CSS [closed]"]
    n13["bob-cli-oj.5.1.2: Day, week, and quarter cards adopt the group row and the derived step row [closed]"]
    n14["bob-cli-oj.5.1.3: Grouped record walk rail and the album card's \"walks by\" pill [closed]"]
    n15["bob-cli-oj.5.1.4: Preview matrix, real-Obsidian e2e runs, and final deploy for the group rail [closed]"]
    n16["bob-cli-oj.6: Group arms and hints in the links walker footer [closed]"]
    n17["bob-cli-oj.7: Album adoption, real-Obsidian proof, and final deploy [closed]"]
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
| [bbugyi200.athena.bob-cli-oj.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-oj.1.md) | [bob-cli-oj.1](bob-cli-oj.1.md) | 0 |
| [bbugyi200.athena.bob-cli-oj.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.2/README.md) | [bob-cli-oj.2](bob-cli-oj.2.md) | 0 |
| [bbugyi200.athena.bob-cli-oj.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-oj.3.md) | [bob-cli-oj.3](bob-cli-oj.3.md) | 0 |
| [bbugyi200.athena.bob-cli-oj.3.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.3.1.1/README.md) | [bob-cli-oj.3.1.1](bob-cli-oj.3.1.1.md) | 1 |
| [bbugyi200.athena.bob-cli-oj.3.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-oj.3.1.2.md) | [bob-cli-oj.3.1.2](bob-cli-oj.3.1.2.md) | 1 |
| [bbugyi200.athena.bob-cli-oj.3.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.3.1.3/README.md) | [bob-cli-oj.3.1.3](bob-cli-oj.3.1.3.md) | 1 |
| [bbugyi200.athena.bob-cli-oj.3.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.3.1.4/README.md) | [bob-cli-oj.3.1.4](bob-cli-oj.3.1.4.md) | 1 |
| [bbugyi200.athena.bob-cli-oj.3.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-oj.3.1.land.md) | [bob-cli-oj.3.1](bob-cli-oj.3.1.md) | 2 |
| [bbugyi200.athena.bob-cli-oj.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-oj.4.md) | [bob-cli-oj.4](bob-cli-oj.4.md) | 0 |
| [bbugyi200.athena.bob-cli-oj.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-oj.5.md) | [bob-cli-oj.5](bob-cli-oj.5.md) | 0 |
| [bbugyi200.athena.bob-cli-oj.5.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.1/README.md) | [bob-cli-oj.5.1.1](bob-cli-oj.5.1.1.md) | 0 |
| [bbugyi200.athena.bob-cli-oj.5.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.2/README.md) | [bob-cli-oj.5.1.2](bob-cli-oj.5.1.2.md) | 0 |
| [bbugyi200.athena.bob-cli-oj.5.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.3/README.md) | [bob-cli-oj.5.1.3](bob-cli-oj.5.1.3.md) | 0 |
| [bbugyi200.athena.bob-cli-oj.5.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.4/README.md) | [bob-cli-oj.5.1.4](bob-cli-oj.5.1.4.md) | 0 |
| [bbugyi200.athena.bob-cli-oj.5.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-oj.5.1.land.md) | [bob-cli-oj.5.1](bob-cli-oj.5.1.md) | 1 |
| [bbugyi200.athena.bob-cli-oj.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.6/README.md) | [bob-cli-oj.6](bob-cli-oj.6.md) | 0 |
| [bbugyi200.athena.bob-cli-oj.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.7/README.md) | [bob-cli-oj.7](bob-cli-oj.7.md) | 0 |
| [bbugyi200.athena.bob-cli-oj.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-oj.8.md) | [bob-cli-oj.8](bob-cli-oj.8.md) | 1 |
| [bbugyi200.athena.bob-cli-oj.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.land/README.md) | [bob-cli-oj](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e11f2a0`](https://github.com/bobs-org/bob-cli/commit/e11f2a0c5e9fa1cb0aefe01a4ccb1ca1785e0af1) | feat(albums): group record walks by declared walk\_by | [bob-cli-oj.3.1.1](bob-cli-oj.3.1.1.md) | 2026-11-21 08:25:36 EST |
| bob-cli | [`ce0dcc5`](https://github.com/bobs-org/bob-cli/commit/ce0dcc54cec50104991b4ad943de0566e7eba2b6) | feat(records): apply grouped walk updates | [bob-cli-oj.3.1.2](bob-cli-oj.3.1.2.md) | 2026-11-21 08:58:17 EST |
| bob-cli | [`66866ea`](https://github.com/bobs-org/bob-cli/commit/66866ea114d6b8eded72d27d66169722d50c6920) | feat(albums): add reversible walk\_by updates to the album writer | [bob-cli-oj.3.1.3](bob-cli-oj.3.1.3.md) | 2026-11-21 09:48:58 EST |
| bob-cli | [`020ad4e`](https://github.com/bobs-org/bob-cli/commit/020ad4e6207f81fd9c633db21c48e1b8efdf3bba) | docs(albums): document grouped record walks | [bob-cli-oj.3.1.4](bob-cli-oj.3.1.4.md) | 2026-11-21 10:15:34 EST |
| bob-cli | [`7ac4fee`](https://github.com/bobs-org/bob-cli/commit/7ac4feeb043503a050e253dfe499da32c9ac1e04) | fix(albums): restore walk\_by at original slot and bind emitted selection | [bob-cli-oj.3.1](bob-cli-oj.3.1.md) | 2026-11-21 11:15:03 EST |
| bob-cli--plans | [`bob-cli--plans@761b2b8`](https://github.com/bobs-org/bob-cli--plans/commit/761b2b8b536aef795ef576ab2a98fb7f7256a9b3) | chore(plans): mark album\_walk\_by epic and landing repairs done | [bob-cli-oj.3.1](bob-cli-oj.3.1.md) | 2026-11-21 11:15:49 EST |
| bob-cli--plans | [`bob-cli--plans@b8a4c00`](https://github.com/bobs-org/bob-cli--plans/commit/b8a4c00646dae5071489f1a2214c3f31a0edf796) | chore(plans): mark group\_rail done after landing bob-cli-oj.5.1 | [bob-cli-oj.5.1](bob-cli-oj.5.1.md) | 2026-11-21 17:12:20 EST |
| bob-cli | [`016cb00`](https://github.com/bobs-org/bob-cli/commit/016cb00845d6e85c9149744eed25208fffac3b1a) | docs(glossary): record grouped walks and group stops in record-note and walker-footer | [bob-cli-oj.8](bob-cli-oj.8.md) | 2026-11-21 20:10:48 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-o6.land][1] | Attribute the bob-cli-ot yaml-done-returns regression to oj.6 commit 7b44b29; need the epic status to route the discovered-issue note | 1 |
| read-by | [agent:bob-cli-oj.2][2] | Need parent epic DECISIONS, notes, and overall scope | 1 |
| read-by | [agent:bob-cli-oj.6][3] | Need sibling phase statuses so I do not redo landed work or collide with group-rail | 1 |
| read-by | [agent:bob-cli-oj.7][4] | Need landed phase notes, versions, and follow-ups before adoption and e2e proof | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-o6.land/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.6/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.7/README.md

<!-- sase:referenced-by:end -->
