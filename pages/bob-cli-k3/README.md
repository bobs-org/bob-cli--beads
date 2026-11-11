# Bead: bob-cli-k3 — Album notes — every record collection hangs under the area it serves

[Bead Pages](../README.md) / bob-cli-k3

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** `bbugyi200.apollo.research.43.linker.w0` · **Assignee:** `bob-cli-k3.land`
**Created:** 2026-11-11 04:56:43 EST
**Plan:** [202611/album\_and\_record\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/album_and_record_notes.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/album_and_record_notes.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 6 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/album_and_record_notes.md

<!-- sase:links:end -->

## Description

Every record note reaches an area of responsibility. Each record collection (eat, podcasts, tv, movies) becomes an album note: `type: "[[album]]"` under its owner area, holding its record schema in frontmatter instead of `config.yml`, de-zorged, and showing a generated, grouped `[!records]` index. Every owner area or project shows a beautiful generated `## Albums` catalog. Records become `type: "[[record]]"` children of their album. Schema and data version together in the vault, a broken album fails alone, and glossary terms for album note and record note are published.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-k3.1](bob-cli-k3.1.md) | Vault-only cleanup — owners, the eat.md de-zorg, and record health | ✓ closed | medium | 2026-11-11 | 0 | 0 |
| [bob-cli-k3.10](bob-cli-k3.10.md) | Link the spending ledger to restaurant records and backfill visited | ◐ in_progress | medium | 2026-11-11 | 1 | 0 |
| [bob-cli-k3.11](bob-cli-k3.11.md) | Retire config-declared records, end-to-end proof, docs audit, and memory | ◐ in_progress | medium | 2026-11-11 | 1 | 0 |
| [bob-cli-k3.2](bob-cli-k3.2.md) | Album recognition, the vault schema registry, and bob albums list and check | ✓ closed | large | 2026-11-11 | 0 | 0 |
| [bob-cli-k3.3](bob-cli-k3.3.md) | Shared host-catalog region engine extracted from notebooks | ✓ closed | medium | 2026-11-11 | 1 | 1 |
| [bob-cli-k3.4](bob-cli-k3.4.md) | Records, capture, and completion read schemas from albums | ✓ closed | large | 2026-11-11 | 1 | 0 |
| [bob-cli-k3.5](bob-cli-k3.5.md) | The generated records index inside each album, rebuilt with every record write | ◐ in_progress | large | 2026-11-11 | 1 | 0 |
| [bob-cli-k3.6](bob-cli-k3.6.md) | The Albums catalog in owner notes, and bob albums create | ◐ in_progress | large | 2026-11-11 | 1 | 0 |
| [bob-cli-k3.7](bob-cli-k3.7.md) | Obsidian album cards, live chips, and the album header | ◐ in_progress | large | 2026-11-11 | 1 | 0 |
| [bob-cli-k3.8](bob-cli-k3.8.md) | Bob Mac Capture presents albums | ✓ closed | medium | 2026-11-11 | 1 | 0 |
| [bob-cli-k3.9](bob-cli-k3.9.md) | Album cutover in the vault, then delete records from chezmoi | ◐ in_progress | medium | 2026-11-11 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-k3: Album notes — every record collection hangs under the area it serves [in_progress]"]
    n1["bob-cli-k3.1: Vault-only cleanup — owners, the eat.md de-zorg, and record health [closed]"]
    n2["bob-cli-k3.10: Link the spending ledger to restaurant records and backfill visited [in_progress]"]
    n3["bob-cli-k3.11: Retire config-declared records, end-to-end proof, docs audit, and memory [in_progress]"]
    n4["bob-cli-k3.2: Album recognition, the vault schema registry, and bob albums list and check [closed]"]
    n5["bob-cli-k3.2.1: Album model — schema parsing, vault registry, and read-only reports [closed]"]
    n6["bob-cli-k3.2.1.1: Parse album declarations through shared record schema validation [closed]"]
    n7["bob-cli-k3.2.1.2: Discover album claims, isolate failures, and integrate the vault snapshot [closed]"]
    n8["bob-cli-k3.2.1.3: Ship albums list/check with complete reports, completion, and docs [closed]"]
    n9["bob-cli-k3.3: Shared host-catalog region engine extracted from notebooks [closed]"]
    n10["bob-cli-k3.4: Records, capture, and completion read schemas from albums [closed]"]
    n11["bob-cli-k3.4.1: Album schemas for records, capture, and completion [closed]"]
    n12["bob-cli-k3.4.1.1: Shared resolved record identity and source-aware rendering [closed]"]
    n13["bob-cli-k3.4.1.2: Album-aware records commands and membership checks [closed]"]
    n14["bob-cli-k3.4.1.3: Capture album records and refuse album task homes [closed]"]
    n15["bob-cli-k3.4.1.4: Album-aware targets and completion [closed]"]
    n16["bob-cli-k3.5: The generated records index inside each album, rebuilt with every record write [in_progress]"]
    n17["bob-cli-k3.5.1: Keep each album's records index current [in_progress]"]
    n18["bob-cli-k3.5.1.1: Render the records index and report its state [closed]"]
    n19["bob-cli-k3.5.1.2: Rebuild the index inside record transactions [closed]"]
    n20["bob-cli-k3.5.1.3: Repair indexes through albums sync and nightly [closed]"]
    n21["bob-cli-k3.6: The Albums catalog in owner notes, and bob albums create [in_progress]"]
    n22["bob-cli-k3.7: Obsidian album cards, live chips, and the album header [in_progress]"]
    n23["bob-cli-k3.8: Bob Mac Capture presents albums [closed]"]
    n24["bob-cli-k3.9: Album cutover in the vault, then delete records from chezmoi [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n4 --> n5
    n5 --> n6
    n5 --> n7
    n5 --> n8
    n0 --> n9
    n0 --> n10
    n10 --> n11
    n11 --> n12
    n11 --> n13
    n11 --> n14
    n11 --> n15
    n0 --> n16
    n16 --> n17
    n17 --> n18
    n17 --> n19
    n17 --> n20
    n0 --> n21
    n0 --> n22
    n0 --> n23
    n0 --> n24
    n1 -.-> n24
    n2 -.-> n3
    n4 -.-> n10
    n6 -.-> n7
    n7 -.-> n8
    n9 -.-> n16
    n10 -.-> n16
    n10 -.-> n23
    n12 -.-> n13
    n12 -.-> n14
    n14 -.-> n15
    n16 -.-> n21
    n18 -.-> n19
    n18 -.-> n20
    n19 -.-> n20
    n21 -.-> n22
    n21 -.-> n24
    n22 -.-> n3
    n23 -.-> n3
    n24 -.-> n2
    n24 -.-> n3
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-k3.2.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-k3.2.1.1.md) | [bob-cli-k3.2.1.1](bob-cli-k3.2.1.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-k3.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-k3.3.md) | [bob-cli-k3.3](bob-cli-k3.3.md) | 1 |
| [bbugyi200.athena.bob-cli-k3.10](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k3.10/README.md) | [bob-cli-k3.10](bob-cli-k3.10.md) | 0 |
| [bbugyi200.athena.bob-cli-k3.11](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k3.11/README.md) | [bob-cli-k3.11](bob-cli-k3.11.md) | 0 |
| [bbugyi200.athena.bob-cli-k3.2.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k3.2.1.2/README.md) | [bob-cli-k3.2.1.2](bob-cli-k3.2.1.2.md) | 1 |
| [bbugyi200.athena.bob-cli-k3.2.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-k3.2.1.3.md) | [bob-cli-k3.2.1.3](bob-cli-k3.2.1.3.md) | 1 |
| [bbugyi200.athena.bob-cli-k3.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-k3.2.1.land.md) | [bob-cli-k3.2.1](bob-cli-k3.2.1.md) | 2 |
| [bbugyi200.athena.bob-cli-k3.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-k3.4.md) | [bob-cli-k3.4](bob-cli-k3.4.md) | 0 |
| [bbugyi200.athena.bob-cli-k3.4.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k3.4.1.1/README.md) | [bob-cli-k3.4.1.1](bob-cli-k3.4.1.1.md) | 1 |
| [bbugyi200.athena.bob-cli-k3.4.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-k3.4.1.2.md) | [bob-cli-k3.4.1.2](bob-cli-k3.4.1.2.md) | 1 |
| [bbugyi200.athena.bob-cli-k3.4.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k3.4.1.3/README.md) | [bob-cli-k3.4.1.3](bob-cli-k3.4.1.3.md) | 1 |
| [bbugyi200.athena.bob-cli-k3.4.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k3.4.1.4/README.md) | [bob-cli-k3.4.1.4](bob-cli-k3.4.1.4.md) | 1 |
| [bbugyi200.athena.bob-cli-k3.4.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-k3.4.1.land.md) | [bob-cli-k3.4.1](bob-cli-k3.4.1.md) | 2 |
| [bbugyi200.athena.bob-cli-k3.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-k3.5.md) | [bob-cli-k3.5](bob-cli-k3.5.md) | 0 |
| [bbugyi200.athena.bob-cli-k3.5.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k3.5.1.1/README.md) | [bob-cli-k3.5.1.1](bob-cli-k3.5.1.1.md) | 1 |
| [bbugyi200.athena.bob-cli-k3.5.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k3.5.1.2/README.md) | [bob-cli-k3.5.1.2](bob-cli-k3.5.1.2.md) | 1 |
| [bbugyi200.athena.bob-cli-k3.5.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k3.5.1.3/README.md) | [bob-cli-k3.5.1.3](bob-cli-k3.5.1.3.md) | 1 |
| [bbugyi200.athena.bob-cli-k3.5.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k3.5.1.land/README.md) | [bob-cli-k3.5.1](bob-cli-k3.5.1.md) | 0 |
| [bbugyi200.athena.bob-cli-k3.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k3.6/README.md) | [bob-cli-k3.6](bob-cli-k3.6.md) | 0 |
| [bbugyi200.athena.bob-cli-k3.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k3.7/README.md) | [bob-cli-k3.7](bob-cli-k3.7.md) | 0 |
| [bbugyi200.athena.bob-cli-k3.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-k3.8.md) | [bob-cli-k3.8](bob-cli-k3.8.md) | 0 |
| [bbugyi200.athena.bob-cli-k3.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k3.9/README.md) | [bob-cli-k3.9](bob-cli-k3.9.md) | 0 |
| [bbugyi200.athena.bob-cli-k3.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k3.land/README.md) | [bob-cli-k3](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f977009`](https://github.com/bobs-org/bob-cli/commit/f977009a26f64775b377c27ed885fdf61ef6f1da) | feat(albums): parse declarations through shared schema validation | [bob-cli-k3.2.1.1](bob-cli-k3.2.1.1.md) | 2026-11-11 06:00:18 EST |
| bob-cli | [`d0ada55`](https://github.com/bobs-org/bob-cli/commit/d0ada555a8b60c74933f9ce4eb3aa8c0469b0d64) | refactor(notebooks): extract shared host-catalog region engine | [bob-cli-k3.3](bob-cli-k3.3.md) | 2026-11-11 06:03:48 EST |
| bob-cli | [`b6f3b92`](https://github.com/bobs-org/bob-cli/commit/b6f3b92c010044e720ebcd75ed47c2f014c6ab0d) | feat(albums): add vault-scoped album registry | [bob-cli-k3.2.1.2](bob-cli-k3.2.1.2.md) | 2026-11-11 06:59:18 EST |
| bob-cli | [`ba9867a`](https://github.com/bobs-org/bob-cli/commit/ba9867a56d0d28b163a480aa9a837e636a2242a2) | feat(albums): add list/check reports, completion, and docs | [bob-cli-k3.2.1.3](bob-cli-k3.2.1.3.md) | 2026-11-11 08:17:41 EST |
| bob-cli | [`ba3f51b`](https://github.com/bobs-org/bob-cli/commit/ba3f51bad3bd491d66e739a895ce4de99149329f) | fix(albums): confine routes, recover nouns, and restore report diagnostics | [bob-cli-k3.2.1](bob-cli-k3.2.1.md) | 2026-11-11 09:11:57 EST |
| bob-cli--plans | [`bob-cli--plans@5335af5`](https://github.com/bobs-org/bob-cli--plans/commit/5335af5dd1df88005093f7e933575f39fdf026ae) | chore(plans): mark album\_model epic plan done | [bob-cli-k3.2.1](bob-cli-k3.2.1.md) | 2026-11-11 09:12:30 EST |
| bob-cli | [`f7332f5`](https://github.com/bobs-org/bob-cli/commit/f7332f5813c2929c2cd2979a755955cc5cf86074) | feat(records): add shared album record context | [bob-cli-k3.4.1.1](bob-cli-k3.4.1.1.md) | 2026-11-11 09:54:13 EST |
| bob-cli | [`8edd5a5`](https://github.com/bobs-org/bob-cli/commit/8edd5a5ffacc4f606b2765a7c81557a321cc078b) | feat(capture)!: per-route album resolution with task-home refusals | [bob-cli-k3.4.1.3](bob-cli-k3.4.1.3.md) | 2026-11-11 11:00:01 EST |
| bob-cli | [`c36e6e7`](https://github.com/bobs-org/bob-cli/commit/c36e6e752d36828f6bd73e09cb095d7c70d25498) | feat(records): add album-aware records commands and membership checks | [bob-cli-k3.4.1.2](bob-cli-k3.4.1.2.md) | 2026-11-11 11:19:55 EST |
| bob-cli | [`3d1c076`](https://github.com/bobs-org/bob-cli/commit/3d1c0763871e992e6aa8ca652eebda69cddf0b26) | feat(capture): use album registry across targets and completion | [bob-cli-k3.4.1.4](bob-cli-k3.4.1.4.md) | 2026-11-11 11:43:11 EST |
| bob-cli | [`6e42159`](https://github.com/bobs-org/bob-cli/commit/6e4215971c02e0f88e12616fee37159fe455f0e1) | feat(capture)!: finish the album consumer landing repairs | [bob-cli-k3.4.1](bob-cli-k3.4.1.md) | 2026-11-11 13:36:26 EST |
| bob-cli--plans | [`bob-cli--plans@2814cf2`](https://github.com/bobs-org/bob-cli--plans/commit/2814cf2080d90274459893f3498694682be87ea1) | docs(plans): mark album\_record\_consumers done after consumer landing | [bob-cli-k3.4.1](bob-cli-k3.4.1.md) | 2026-11-11 13:37:21 EST |
| bob-cli | [`1f4c945`](https://github.com/bobs-org/bob-cli/commit/1f4c94571454ed9307094a677f69b31cddc30600) | feat(albums): render the records index and report its state | [bob-cli-k3.5.1.1](bob-cli-k3.5.1.1.md) | 2026-11-11 14:38:15 EST |
| bob-cli | [`b79ea37`](https://github.com/bobs-org/bob-cli/commit/b79ea376ff57017d460c83b5f08e7f8153860be7) | feat(albums): rebuild the records index inside record transactions | [bob-cli-k3.5.1.2](bob-cli-k3.5.1.2.md) | 2026-11-11 16:13:47 EST |
| bob-cli | [`6352824`](https://github.com/bobs-org/bob-cli/commit/6352824bffd7db5d2d22950ed83f101c7b8ae4de) | feat(albums): sync generated record indexes | [bob-cli-k3.5.1.3](bob-cli-k3.5.1.3.md) | 2026-11-11 17:22:22 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:research.47.cdx][1] | Read album foundation epic and its current implementation constraints for bank album design | 1 |
| read-by | [agent:research.47.cld][2] | Understand the albums epic to design a bank album | 1 |
| read-by | [agent:research.47.final][3] | Check album epic status for bank album consolidation | 1 |
| read-by | [agent:research.47.gem][4] | research bank album design context | 1 |
| read-by | [agent:research.47.grk][5] | Need the albums epic context before designing a bank album | 1 |
| read-by | [agent:research.47.mus][6] | Research bank album needs album epic context | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.47.cdx/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.47.cld/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.47.final/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.47.gem/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.47.grk/README.md
[6]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.47.mus/README.md

<!-- sase:referenced-by:end -->
