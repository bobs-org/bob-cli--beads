# Bead: bob-cli-gm — Several @file+id targets on one capture line

[Bead Pages](../README.md) / bob-cli-gm

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.17k](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.17k.md) · **Assignee:** `bob-cli-gm.land`
**Created:** 2026-11-03 13:55:33 EST
**Plan:** [202611/capture\_multi\_target.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_multi_target.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/capture_multi_target.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_multi_target.md

<!-- sase:links:end -->

## Description

One capture line may name several existing tasks with adjacent `@route+block-id` markers. Its note text, the bullets below it, and every operation on the line (clipboard notes, `s:`/`$`, `#type`, `&`/`*`/`~`, Ensure Next, `!` toggle, drawers) then apply to each named task in one atomic capture. `bob capture`, `capture-parse`, `capture-complete`, and `capture-rewrite` agree on the grammar, and Bob Mac Capture keeps working unchanged.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-gm.1](bob-cli-gm.1.md) | Target-run grammar in both resolvers, fan-out, and grammar bump | ✓ closed | large | 2026-11-03 | 1 | 0 |
| [bob-cli-gm.2](bob-cli-gm.2.md) | Planner, output, and capture contract for fan-out groups | ◐ in_progress | medium | 2026-11-03 | 1 | 0 |
| [bob-cli-gm.3](bob-cli-gm.3.md) | Completion, rewrite, and @@ absorption inside target runs | ✓ closed | medium | 2026-11-03 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-gm: Several @file+id targets on one capture line [in_progress]"]
    n1["bob-cli-gm.1: Target-run grammar in both resolvers, fan-out, and grammar bump [closed]"]
    n2["bob-cli-gm.1.1: Complete capture target-run grammar in bounded phases [closed]"]
    n3["bob-cli-gm.1.1.1: Shared target selection and source-preserving member views [closed]"]
    n4["bob-cli-gm.1.1.2: Execution member resolution and draft fan-out [closed]"]
    n5["bob-cli-gm.1.1.3: Editor member semantics and targets JSON [closed]"]
    n6["bob-cli-gm.1.1.4: Activate both parsers and publish the grammar contract [closed]"]
    n7["bob-cli-gm.2: Planner, output, and capture contract for fan-out groups [in_progress]"]
    n8["bob-cli-gm.3: Completion, rewrite, and @@ absorption inside target runs [closed]"]
    n0 --> n1
    n1 --> n2
    n2 --> n3
    n2 --> n4
    n2 --> n5
    n2 --> n6
    n0 --> n7
    n0 --> n8
    n1 -.-> n7
    n1 -.-> n8
    n3 -.-> n4
    n4 -.-> n5
    n5 -.-> n6
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-gm.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-gm.1.md) | [bob-cli-gm.1](bob-cli-gm.1.md) | 0 |
| [bbugyi200.athena.bob-cli-gm.1.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gm.1.1.1/README.md) | [bob-cli-gm.1.1.1](bob-cli-gm.1.1.1.md) | 1 |
| [bbugyi200.athena.bob-cli-gm.1.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gm.1.1.2/README.md) | [bob-cli-gm.1.1.2](bob-cli-gm.1.1.2.md) | 1 |
| [bbugyi200.athena.bob-cli-gm.1.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gm.1.1.3/README.md) | [bob-cli-gm.1.1.3](bob-cli-gm.1.1.3.md) | 1 |
| [bbugyi200.athena.bob-cli-gm.1.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-gm.1.1.4.md) | [bob-cli-gm.1.1.4](bob-cli-gm.1.1.4.md) | 1 |
| [bbugyi200.athena.bob-cli-gm.1.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-gm.1.1.land.md) | [bob-cli-gm.1.1](bob-cli-gm.1.1.md) | 1 |
| [bbugyi200.athena.bob-cli-gm.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gm.2/README.md) | [bob-cli-gm.2](bob-cli-gm.2.md) | 0 |
| [bbugyi200.athena.bob-cli-gm.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gm.3/README.md) | [bob-cli-gm.3](bob-cli-gm.3.md) | 1 |
| [bbugyi200.athena.bob-cli-gm.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gm.land/README.md) | [bob-cli-gm](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d1f3484`](https://github.com/bobs-org/bob-cli/commit/d1f3484200081294a96bcd029654b7545d7b7305) | feat(capture): add shared target-run selection staging | [bob-cli-gm.1.1.1](bob-cli-gm.1.1.1.md) | 2026-11-03 17:24:23 EST |
| bob-cli | [`a7c4b07`](https://github.com/bobs-org/bob-cli/commit/a7c4b07fe07fa809a4f22b3aafdff94b0012134d) | feat(capture): fan out selected target runs | [bob-cli-gm.1.1.2](bob-cli-gm.1.1.2.md) | 2026-11-03 18:09:46 EST |
| bob-cli | [`6a5b69b`](https://github.com/bobs-org/bob-cli/commit/6a5b69b081ee8d11ebc191d233aebe6f4ebe15fd) | feat(capture): combine editor target runs into one item with targets | [bob-cli-gm.1.1.3](bob-cli-gm.1.1.3.md) | 2026-11-03 18:49:25 EST |
| bob-cli | [`c341649`](https://github.com/bobs-org/bob-cli/commit/c341649a46ad1dd58f81a0be4f3930b9315964c8) | feat(capture): activate multi-target capture runs | [bob-cli-gm.1.1.4](bob-cli-gm.1.1.4.md) | 2026-11-03 19:53:10 EST |
| bob-cli | [`ebedfca`](https://github.com/bobs-org/bob-cli/commit/ebedfca8e666a9a79e9cc2989aca0a6b78edd983) | feat(capture)!: complete target-run grammar and landing | [bob-cli-gm.1.1](bob-cli-gm.1.1.md) | 2026-11-03 21:13:52 EST |
| bob-cli | [`d19a8d9`](https://github.com/bobs-org/bob-cli/commit/d19a8d92f9641416d936697445deb19086af851c) | feat(capture): complete and rewrite inside target runs | [bob-cli-gm.3](bob-cli-gm.3.md) | 2026-11-03 21:59:49 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:research.36.final][1] | Check multi-target epic decisions section for split_edges choice | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.36.final/README.md

<!-- sase:referenced-by:end -->
