# Bead: bob-cli-9u — Underline emphasis inside highlights

[Bead Pages](../README.md) / bob-cli-9u

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.4z.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.4z.linker.w0.md) · **Assignee:** `bob-cli-9u.land`
**Created:** 2026-10-19 11:48:18 EDT
**Plan:** [202610/underline\_emphasis.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/underline_emphasis.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/underline_emphasis.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/underline_emphasis.md

<!-- sase:links:end -->

## Description

An underline drawn inside a highlight renders as bold emphasis inside that highlight's quote in Obsidian, bob ref show, and the Bob Mac Capture preview. Its comment, tasks, and image notes join the highlight, anchors stay valid, and nothing is written to the PDF or the sidecar.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-9u.1](bob-cli-9u.1.md) | Classify, match, and fold underlines into their highlights | ✓ closed | medium | 2026-10-19 | 1 | 1 |
| [bob-cli-9u.2](bob-cli-9u.2.md) | Scan counters, terminal bold, docs, and the Obsidian snippet | ✓ closed | small | 2026-10-19 | 1 | 1 |
| [bob-cli-9u.3](bob-cli-9u.3.md) | Emphasis-aware quote preview in Bob Mac Capture | ✓ closed | small | 2026-10-19 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-9u: Underline emphasis inside highlights [in_progress]"]
    n1["bob-cli-9u.1: Classify, match, and fold underlines into their highlights [closed]"]
    n2["bob-cli-9u.2: Scan counters, terminal bold, docs, and the Obsidian snippet [closed]"]
    n3["bob-cli-9u.3: Emphasis-aware quote preview in Bob Mac Capture [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n1 -.-> n2
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-9u.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9u.1/README.md) | [bob-cli-9u.1](bob-cli-9u.1.md) | 1 |
| [bbugyi200.athena.bob-cli-9u.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-9u.2.md) | [bob-cli-9u.2](bob-cli-9u.2.md) | 1 |
| [bbugyi200.athena.bob-cli-9u.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9u.3/README.md) | [bob-cli-9u.3](bob-cli-9u.3.md) | 0 |
| [bbugyi200.athena.bob-cli-9u.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9u.land/README.md) | [bob-cli-9u](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a2638aa`](https://github.com/bobs-org/bob-cli/commit/a2638aa92e4da62e6733af86fcc01708df7da1ef) | feat(highlights): fold underlines into highlight quotes | [bob-cli-9u.1](bob-cli-9u.1.md) | 2026-10-19 12:25:38 EDT |
| bob-cli | [`1dc6fe0`](https://github.com/bobs-org/bob-cli/commit/1dc6fe0606948c8741bf0dcd217a51155a1d6726) | feat(ref): report and render underline emphasis | [bob-cli-9u.2](bob-cli-9u.2.md) | 2026-10-19 12:50:11 EDT |
