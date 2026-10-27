# Bead: bob-cli-dd — Backlog batch B3: Mac and plugin flakes, plus lossless theme rename

[Bead Pages](../README.md) / bob-cli-dd

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-da.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-da.land.md) · **Assignee:** `bob-cli-dd.land`
**Created:** 2026-10-27 18:53:10 EDT
**Plan:** [202610/backlog\_batch\_b3.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch_b3.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/backlog_batch_b3.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch_b3.md

<!-- sase:links:end -->

## Description

Resolve bob-cli-d4, bob-cli-d9, and bob-cli-dc with reproducible verification, then continue the bounded backlog chain.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-dd.1](bob-cli-dd.1.md) | Stabilize the Highlights current-tab test | ◐ in_progress | large | 2026-10-27 | 1 | 0 |
| [bob-cli-dd.2](bob-cli-dd.2.md) | Prove FIFO writers and overlapping readers without a wall-clock race | ✓ closed | medium | 2026-10-27 | 1 | 0 |
| [bob-cli-dd.3](bob-cli-dd.3.md) | Preserve every byte outside renamed theme spans | ✓ closed | small | 2026-10-27 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-dd: Backlog batch B3: Mac and plugin flakes, plus lossless theme rename [in_progress]"]
    n1["bob-cli-dd.1: Stabilize the Highlights current-tab test [in_progress]"]
    n2["bob-cli-dd.2: Prove FIFO writers and overlapping readers without a wall-clock race [closed]"]
    n3["bob-cli-dd.3: Preserve every byte outside renamed theme spans [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-dd.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-dd.1.md) | [bob-cli-dd.1](bob-cli-dd.1.md) | 0 |
| [bbugyi200.athena.bob-cli-dd.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-dd.2/README.md) | [bob-cli-dd.2](bob-cli-dd.2.md) | 0 |
| [bbugyi200.athena.bob-cli-dd.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-dd.3/README.md) | [bob-cli-dd.3](bob-cli-dd.3.md) | 1 |
| [bbugyi200.athena.bob-cli-dd.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-dd.land/README.md) | [bob-cli-dd](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0421192`](https://github.com/bobs-org/bob-cli/commit/0421192684d525f556f44aa35a6e5ff61ef3660b) | fix(themes): preserve every byte outside renamed theme spans | [bob-cli-dd.3](bob-cli-dd.3.md) | 2026-10-27 19:12:02 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-dd.2][1] | Need epic DECISIONS before implementing phase | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-dd.2/README.md

<!-- sase:referenced-by:end -->
