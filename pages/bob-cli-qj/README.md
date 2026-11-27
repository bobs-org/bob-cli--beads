# Bead: bob-cli-qj — Rename the article note type to prose

[Bead Pages](../README.md) / bob-cli-qj

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.6i.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.6i.linker.w0.md) · **Assignee:** `bob-cli-qj.land`
**Created:** 2026-11-26 10:56:26 EST
**Plan:** [202611/prose\_note\_type.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/prose_note_type.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/prose_note_type.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 14 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/prose_note_type.md

<!-- sase:links:end -->

## Description

The Bob note type for authored writing is named prose everywhere a person reads it: the type link, the bob prose CLI, Bob Prose in Obsidian, the docs, and the vault. Every legacy article note, bob articles call, plugin id, and JSON consumer keeps working unchanged, and prose-section extract/inline is planned on top of the rename.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-qj.1](bob-cli-qj.1.md) | Rename the Rust article engine to prose | ✓ closed | small | 2026-11-26 | 1 | 1 |
| [bob-cli-qj.2](bob-cli-qj.2.md) | bob prose with permanent legacy aliases | ✓ closed | medium | 2026-11-26 | 1 | 1 |
| [bob-cli-qj.3](bob-cli-qj.3.md) | Bob Prose in Obsidian | ✓ closed | medium | 2026-11-26 | 1 | 0 |
| [bob-cli-qj.4](bob-cli-qj.4.md) | Host gate, vault cutover, and canonical plugin calls | ◐ in_progress | small | 2026-11-26 | 1 | 1 |
| [bob-cli-qj.5](bob-cli-qj.5.md) | Plan prose-section extract and inline | ◐ in_progress | xlarge | 2026-11-26 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-qj: Rename the article note type to prose [in_progress]"]
    n1["bob-cli-qj.1: Rename the Rust article engine to prose [closed]"]
    n2["bob-cli-qj.2: bob prose with permanent legacy aliases [closed]"]
    n3["bob-cli-qj.3: Bob Prose in Obsidian [closed]"]
    n4["bob-cli-qj.4: Host gate, vault cutover, and canonical plugin calls [in_progress]"]
    n5["bob-cli-qj.5: Plan prose-section extract and inline [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n1 -.-> n2
    n2 -.-> n3
    n2 -.-> n4
    n3 -.-> n4
    n4 -.-> n5
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-qj.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qj.1/README.md) | [bob-cli-qj.1](bob-cli-qj.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-qj.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qj.2/README.md) | [bob-cli-qj.2](bob-cli-qj.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-qj.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qj.3/README.md) | [bob-cli-qj.3](bob-cli-qj.3.md) | 0 |
| [bbugyi200.apollo.bob-cli-qj.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qj.4/README.md) | [bob-cli-qj.4](bob-cli-qj.4.md) | 1 |
| [bbugyi200.apollo.bob-cli-qj.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qj.5/README.md) | [bob-cli-qj.5](bob-cli-qj.5.md) | 0 |
| [bbugyi200.apollo.bob-cli-qj.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qj.land/README.md) | [bob-cli-qj](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`cf414ce`](https://github.com/bobs-org/bob-cli/commit/cf414ce15c5489203abf81d308d9359d30214510) | refactor(prose): rename the article engine module to prose | [bob-cli-qj.1](bob-cli-qj.1.md) | 2026-11-26 12:15:08 EST |
| bob-cli | [`4168e20`](https://github.com/bobs-org/bob-cli/commit/4168e2013a35cf08e11858c2d66a61d60f5f8a8b) | feat(prose): make prose the canonical note type and CLI | [bob-cli-qj.2](bob-cli-qj.2.md) | 2026-11-26 14:48:41 EST |
| bob-cli | [`16a2497`](https://github.com/bobs-org/bob-cli/commit/16a2497d0a73f8497220a656116eaf311c08d246) | docs(decisions): cite the prose-cli commit in prose-notes-are-owned-prose | [bob-cli-qj.4](bob-cli-qj.4.md) | 2026-11-27 06:34:53 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-qj.1][1] | need epic scope | 1 |
| read-by | [agent:research.6k.cdx][2] | Determine active epic contracts and overlaps for prose and notebook cards | 1 |
| read-by | [agent:research.6k.cld][3] | Research prose/notebook property cards; must understand in-progress epic to plan parallel work | 1 |
| read-by | [agent:research.6k.final][4] | Lead researcher verifying live epic phase status for the consolidated prose/notebook card sequencing recommendation | 1 |
| read-by | [agent:research.6k.gem][5] | Inspect in-progress epic bob-cli-qj for parallel coordination analysis | 1 |
| read-by | [agent:research.6k.grk][6] | Need qj prose-rename epic scope to judge parallel implementation with prose/notebook cards | 1 |
| read-by | [agent:research.6k.mus][7] | prose/notebook card research: check parallel epic scope | 1 |
| read-by | [agent:research.6l.cld][8] | Check qj phase states for ref card coordination | 1 |
| read-by | [agent:research.6m.cdx][9] | Research independent cabinet implementation and overlap with active epics | 1 |
| read-by | [agent:research.6m.cld][10] | Assess coordination with cabinets research | 1 |
| read-by | [agent:research.6m.final][11] | Refresh epic phase snapshot for consolidated cabinets research | 4 |
| read-by | [agent:research.6m.gem][12] | Understand active epic scope, files, and status for parallel cabinet implementation analysis | 1 |
| read-by | [agent:research.6m.grk][13] | Cite sibling epic scope and out-of-scope catalog work before recommending a cabinets epic | 2 |
| read-by | [agent:research.6m.mus][14] | Research cabinet design parallel coordination with in-progress epics | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qj.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.6k.cdx/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.6k.cld/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.6k.final/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.6k.gem/README.md
[6]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.6k.grk/README.md
[7]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.6k.mus/README.md
[8]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.6l.cld/README.md
[9]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.6m.cdx/README.md
[10]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.6m.cld/README.md
[11]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.6m.final/README.md
[12]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.6m.gem/README.md
[13]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.6m.grk/README.md
[14]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.6m.mus/README.md

<!-- sase:referenced-by:end -->
