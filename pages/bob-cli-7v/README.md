# Bead: bob-cli-7v — Several URLs, one reference: multi-URL bob ref create collections

[Bead Pages](../README.md) / bob-cli-7v

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.10k](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.10k.md) · **Assignee:** `bob-cli-7v.land`
**Created:** 2026-10-15 12:30:28 EDT
**Plan:** [202610/ref\_create\_multi\_url\_collections.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_create_multi_url_collections.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/ref_create_multi_url_collections.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_create_multi_url_collections.md

<!-- sase:links:end -->

## Description

`bob ref create URL URL…` merges 2 to 20 web articles, in argument order, into one Highlights-ready PDF and one reference. The PDF has a contents page, one bookmark per article, and continuous page numbers. The name comes from `-N` or from the words every URL's slug shares. The command is all-or-nothing and fails fast, before any network call, whenever no trustworthy name exists.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-7v.1](bob-cli-7v.1.md) | List-aware import dedupe for source\_url and url lists | ✓ closed | small | 2026-10-15 | 1 | 1 |
| [bob-cli-7v.2](bob-cli-7v.2.md) | Pure collection naming and metadata rules | ✓ closed | medium | 2026-10-15 | 1 | 1 |
| [bob-cli-7v.3](bob-cli-7v.3.md) | Adapter render:false capture, compose op, and the collection layout | ✓ closed | medium | 2026-10-15 | 1 | 1 |
| [bob-cli-7v.4](bob-cli-7v.4.md) | Variadic TARGET, fail-fast validation, and collection overlap policy | ✓ closed | medium | 2026-10-15 | 1 | 1 |
| [bob-cli-7v.5](bob-cli-7v.5.md) | Collection route - classify, capture, compose, stamp, install, report | ✓ closed | medium | 2026-10-15 | 1 | 1 |
| [bob-cli-7v.6](bob-cli-7v.6.md) | Narrate and attach collections with --listen | ✓ closed | small | 2026-10-15 | 1 | 1 |
| [bob-cli-7v.7](bob-cli-7v.7.md) | Docs, live verification, and follow-ups | ✓ closed | small | 2026-10-15 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-7v: Several URLs, one reference: multi-URL bob ref create collections [in_progress]"]
    n1["bob-cli-7v.1: List-aware import dedupe for source_url and url lists [closed]"]
    n2["bob-cli-7v.2: Pure collection naming and metadata rules [closed]"]
    n3["bob-cli-7v.3: Adapter render:false capture, compose op, and the collection layout [closed]"]
    n4["bob-cli-7v.4: Variadic TARGET, fail-fast validation, and collection overlap policy [closed]"]
    n5["bob-cli-7v.5: Collection route - classify, capture, compose, stamp, install, report [closed]"]
    n6["bob-cli-7v.6: Narrate and attach collections with --listen [closed]"]
    n7["bob-cli-7v.7: Docs, live verification, and follow-ups [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n0 --> n7
    n1 -.-> n4
    n2 -.-> n4
    n3 -.-> n5
    n4 -.-> n5
    n5 -.-> n6
    n6 -.-> n7
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-7v.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-7v.1/README.md) | [bob-cli-7v.1](bob-cli-7v.1.md) | 1 |
| [bbugyi200.athena.bob-cli-7v.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-7v.2.md) | [bob-cli-7v.2](bob-cli-7v.2.md) | 1 |
| [bbugyi200.athena.bob-cli-7v.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-7v.3/README.md) | [bob-cli-7v.3](bob-cli-7v.3.md) | 1 |
| [bbugyi200.athena.bob-cli-7v.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-7v.4/README.md) | [bob-cli-7v.4](bob-cli-7v.4.md) | 1 |
| [bbugyi200.athena.bob-cli-7v.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-7v.5.md) | [bob-cli-7v.5](bob-cli-7v.5.md) | 1 |
| [bbugyi200.athena.bob-cli-7v.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-7v.6.md) | [bob-cli-7v.6](bob-cli-7v.6.md) | 1 |
| [bbugyi200.athena.bob-cli-7v.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-7v.7.md) | [bob-cli-7v.7](bob-cli-7v.7.md) | 1 |
| [bbugyi200.athena.bob-cli-7v.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-7v.land/README.md) | [bob-cli-7v](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`47e85f6`](https://github.com/bobs-org/bob-cli/commit/47e85f65e00dc953c25416b475b21fe0ee4bea92) | feat(ref): dedupe list-valued source URLs | [bob-cli-7v.1](bob-cli-7v.1.md) | 2026-10-15 12:39:19 EDT |
| bob-cli | [`63ec1ca`](https://github.com/bobs-org/bob-cli/commit/63ec1ca5f138da48c3e244a4745006ad272ecf6f) | feat(ref): add collection naming and metadata rules | [bob-cli-7v.2](bob-cli-7v.2.md) | 2026-10-15 12:57:34 EDT |
| bob-cli | [`e104962`](https://github.com/bobs-org/bob-cli/commit/e10496251059137f53dece8f98543e24d5fae283) | feat(web-clip): add render:false capture and collection compose | [bob-cli-7v.3](bob-cli-7v.3.md) | 2026-10-15 12:58:59 EDT |
| bob-cli | [`5feaaac`](https://github.com/bobs-org/bob-cli/commit/5feaaac1a322b5756d3469464d866ca85a89bcae) | feat(highlights-ref): add multi-url collection gate | [bob-cli-7v.4](bob-cli-7v.4.md) | 2026-10-15 13:22:20 EDT |
| bob-cli | [`9bdb0bd`](https://github.com/bobs-org/bob-cli/commit/9bdb0bd9eadbb0382f06f5815ebc51019e94ae9a) | feat(highlights-ref): wire the multi-url collection capture pipeline | [bob-cli-7v.5](bob-cli-7v.5.md) | 2026-10-15 13:57:29 EDT |
| bob-cli | [`f596bf3`](https://github.com/bobs-org/bob-cli/commit/f596bf33154e1c0440820aab46c91b92357799a7) | feat(ref): add collection listen and attach support | [bob-cli-7v.6](bob-cli-7v.6.md) | 2026-10-15 14:41:57 EDT |
| bob-cli | [`dad02a2`](https://github.com/bobs-org/bob-cli/commit/dad02a2f6e308ca8492759a967e17658d140f6b4) | docs(ref): document multi-url collections | [bob-cli-7v.7](bob-cli-7v.7.md) | 2026-10-15 15:07:15 EDT |
