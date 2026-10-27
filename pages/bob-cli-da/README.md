# Bead: bob-cli-da — Backlog batch B2: macOS completion flake, Mermaid class, vault-format docs, and assets split

[Bead Pages](../README.md) / bob-cli-da

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-d7.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-d7.land.md) · **Assignee:** `bob-cli-da.land`
**Created:** 2026-10-27 16:30:19 EDT
**Plan:** [202610/backlog\_batch\_b2.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch_b2.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/backlog_batch_b2.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch_b2.md

<!-- sase:links:end -->

## Description

Resolve the four most important remaining bob-cli beads after batch A1: re-check the macOS completion flake against the new deadline pin, restore the web-clip Mermaid classification, correct the vault-format walk order, and decide the assets-crate split before the package breaches its cap. The lander then starts the next backlog epic, so the chain continues until no open task beads remain.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-da.1](bob-cli-da.1.md) | Re-check the macOS aliases completion flake after the deadline pin | ✓ closed | large | 2026-10-27 | 1 | 0 |
| [bob-cli-da.2](bob-cli-da.2.md) | Keep language-mermaid through web-clip extraction | ✓ closed | medium | 2026-10-27 | 1 | 1 |
| [bob-cli-da.3](bob-cli-da.3.md) | Correct the vault-format walk order and check the page | ✓ closed | small | 2026-10-27 | 1 | 1 |
| [bob-cli-da.4](bob-cli-da.4.md) | Split embedded assets before the package breaches its cap | ✓ closed | large | 2026-10-27 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-da: Backlog batch B2: macOS completion flake, Mermaid class, vault-format docs, and assets split [in_progress]"]
    n1["bob-cli-da.1: Re-check the macOS aliases completion flake after the deadline pin [closed]"]
    n2["bob-cli-da.2: Keep language-mermaid through web-clip extraction [closed]"]
    n3["bob-cli-da.3: Correct the vault-format walk order and check the page [closed]"]
    n4["bob-cli-da.4: Split embedded assets before the package breaches its cap [closed]"]
    n5["bob-cli-da.4.1: Split embedded assets into a release-managed workspace crate [closed]"]
    n6["bob-cli-da.4.1.1: Move embedded payloads and verify both Cargo packages [closed]"]
    n7["bob-cli-da.4.1.2: Integrate the assets crate with the daily release train [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n4 --> n5
    n5 --> n6
    n5 --> n7
    n6 -.-> n7
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-da.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-da.1.md) | [bob-cli-da.1](bob-cli-da.1.md) | 0 |
| [bbugyi200.athena.bob-cli-da.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-da.2.md) | [bob-cli-da.2](bob-cli-da.2.md) | 1 |
| [bbugyi200.athena.bob-cli-da.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-da.3/README.md) | [bob-cli-da.3](bob-cli-da.3.md) | 1 |
| [bbugyi200.athena.bob-cli-da.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-da.4.md) | [bob-cli-da.4](bob-cli-da.4.md) | 0 |
| [bbugyi200.athena.bob-cli-da.4.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-da.4.1.1/README.md) | [bob-cli-da.4.1.1](bob-cli-da.4.1.1.md) | 1 |
| [bbugyi200.athena.bob-cli-da.4.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-da.4.1.2.md) | [bob-cli-da.4.1.2](bob-cli-da.4.1.2.md) | 1 |
| [bbugyi200.athena.bob-cli-da.4.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-da.4.1.land.md) | [bob-cli-da.4.1](bob-cli-da.4.1.md) | 1 |
| [bbugyi200.athena.bob-cli-da.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-da.land/README.md) | [bob-cli-da](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4fd8291`](https://github.com/bobs-org/bob-cli/commit/4fd82919009fa061ced90434f8033528c9eb6f85) | docs(freshness): correct vault walk order | [bob-cli-da.3](bob-cli-da.3.md) | 2026-10-27 16:40:02 EDT |
| bob-cli | [`b63e5a0`](https://github.com/bobs-org/bob-cli/commit/b63e5a046f4d03de6aa38ce080b015447ad305c5) | feat(assets)!: split embedded payloads into bob-obsidian-assets crate | [bob-cli-da.4.1.1](bob-cli-da.4.1.1.md) | 2026-10-27 17:12:31 EDT |
| bob-cli | [`6b0a30b`](https://github.com/bobs-org/bob-cli/commit/6b0a30bf7b6d18d568f8006088041848d046f976) | fix(web-ref): keep language-mermaid through Defuddle extraction | [bob-cli-da.2](bob-cli-da.2.md) | 2026-10-27 17:20:52 EDT |
| bob-cli | [`3cc6351`](https://github.com/bobs-org/bob-cli/commit/3cc6351158e074791330ad539761ad9dbcadd2f6) | feat(release): integrate bob-obsidian-assets with the daily train | [bob-cli-da.4.1.2](bob-cli-da.4.1.2.md) | 2026-10-27 17:59:20 EDT |
| bob-cli | [`232d68c`](https://github.com/bobs-org/bob-cli/commit/232d68c0058bed3d83af0f714901bd2067ad039f) | test(release): cover split package checks and clarify release docs | [bob-cli-da.4.1](bob-cli-da.4.1.md) | 2026-10-27 18:42:58 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-da.4.1.1][1] | Check epic DECISIONS before closing phase | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-da.4.1.1/README.md

<!-- sase:referenced-by:end -->
