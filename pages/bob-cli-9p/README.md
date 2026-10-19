# Bead: bob-cli-9p — Continuation highlights: a \`\<\` note folds a highlight into the one before it

[Bead Pages](../README.md) / bob-cli-9p

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.4u.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.4u.linker.w0.md) · **Assignee:** `bob-cli-9p.land`
**Created:** 2026-10-19 07:59:12 EDT
**Plan:** [202610/highlight\_continuations.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/highlight_continuations.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/highlight_continuations.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/highlight_continuations.md

<!-- sase:links:end -->

## Description

A Highlights note that starts with `<` makes `bob ref` render that highlight and its notes as one quote with the highlight before it, across pages or within a paragraph. Block identity, tasks, and published anchors stay stable. A marker that cannot merge stays visible and is counted.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-9p.1](bob-cli-9p.1.md) | Parse, plan, and render continuation groups | ✓ closed | medium | 2026-10-19 | 1 | 1 |
| [bob-cli-9p.2](bob-cli-9p.2.md) | Continuation counters, scan output, and docs | ◐ in_progress | small | 2026-10-19 | 1 | 0 |
| [bob-cli-9p.3](bob-cli-9p.3.md) | Plural page labels in Bob Mac Capture | ✓ closed | xsmall | 2026-10-19 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-9p: Continuation highlights: a `&lt;` note folds a highlight into the one before it [in_progress]"]
    n1["bob-cli-9p.1: Parse, plan, and render continuation groups [closed]"]
    n2["bob-cli-9p.2: Continuation counters, scan output, and docs [in_progress]"]
    n3["bob-cli-9p.3: Plural page labels in Bob Mac Capture [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n1 -.-> n2
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-9p.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9p.1/README.md) | [bob-cli-9p.1](bob-cli-9p.1.md) | 1 |
| [bbugyi200.athena.bob-cli-9p.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9p.2/README.md) | [bob-cli-9p.2](bob-cli-9p.2.md) | 0 |
| [bbugyi200.athena.bob-cli-9p.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9p.3/README.md) | [bob-cli-9p.3](bob-cli-9p.3.md) | 0 |
| [bbugyi200.athena.bob-cli-9p.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9p.land/README.md) | [bob-cli-9p](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`3924abc`](https://github.com/bobs-org/bob-cli/commit/3924abc88db68f64353544440dda57687c719782) | feat(highlights): fold continuation highlights at render time | [bob-cli-9p.1](bob-cli-9p.1.md) | 2026-10-19 08:37:12 EDT |
