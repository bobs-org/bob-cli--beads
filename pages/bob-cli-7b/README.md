# Bead: bob-cli-7b — Capture links a dependency-blocked task by dropping its open prerequisites

[Bead Pages](../README.md) / bob-cli-7b

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.7c.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.7c.w0.md) · **Assignee:** `bob-cli-7b.land`
**Created:** 2026-10-13 08:12:08 EDT
**Plan:** [202610/capture\_link\_drops\_blocking\_deps.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_link_drops_blocking_deps.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/capture_link_drops_blocking_deps.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_link_drops_blocking_deps.md

<!-- sase:links:end -->

## Description

Typing an existing-task link gesture (`@route:id`, `^route:id`, `@route+id`, `@route+id!`, `@route:id=x…`) in `bob capture` or Bob Mac Capture on a task that is Blocked only by its own open prerequisites removes those prerequisites from its Depends-On line and then performs the gesture, while every case where dropping is unsafe keeps today's consumption and says why.

## Notes

[2026-10-13T13:59:51Z · bryanbugyi34@gmail.com] Pretty sure the changes made by this epic caused the bob-mac-capture build to fail. See the partial error in the 🔒 bob\_mac\_capture\_error.txt file for context.

## Attachments

- 🔒 bob\_mac\_capture\_error.txt · text/plain · 11.9141 KiB (private attachment)

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-7b.1](bob-cli-7b.1.md) | Contract, dependency-drop writer, and the solo link gesture | ✓ closed | medium | 2026-10-13 | 1 | 1 |
| [bob-cli-7b.2](bob-cli-7b.2.md) | Toggle, Ensure Next, and link-then-close adopt the drop | ✓ closed | medium | 2026-10-13 | 1 | 1 |
| [bob-cli-7b.3](bob-cli-7b.3.md) | Bob Mac Capture presents dropped and refused prerequisites | ✓ closed | medium | 2026-10-13 | 1 | 0 |
| [bob-cli-7b.4](bob-cli-7b.4.md) | Decision record, supersession marks, and docs sweep | ◐ in_progress | small | 2026-10-13 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-7b: Capture links a dependency-blocked task by dropping its open prerequisites [in_progress]"]
    n1["bob-cli-7b.1: Contract, dependency-drop writer, and the solo link gesture [closed]"]
    n2["bob-cli-7b.2: Toggle, Ensure Next, and link-then-close adopt the drop [closed]"]
    n3["bob-cli-7b.3: Bob Mac Capture presents dropped and refused prerequisites [closed]"]
    n4["bob-cli-7b.4: Decision record, supersession marks, and docs sweep [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n1 -.-> n2
    n1 -.-> n3
    n2 -.-> n4
    n3 -.-> n4
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-7b.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-7b.1.md) | [bob-cli-7b.1](bob-cli-7b.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-7b.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-7b.2/README.md) | [bob-cli-7b.2](bob-cli-7b.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-7b.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-7b.3/README.md) | [bob-cli-7b.3](bob-cli-7b.3.md) | 0 |
| [bbugyi200.apollo.bob-cli-7b.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-7b.4/README.md) | [bob-cli-7b.4](bob-cli-7b.4.md) | 0 |
| [bbugyi200.apollo.bob-cli-7b.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-7b.land/README.md) | [bob-cli-7b](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`92515f1`](https://github.com/bobs-org/bob-cli/commit/92515f1bb8565fa7d6116e4581911b9f45e880bb) | feat(capture): support dependency-drop link gestures | [bob-cli-7b.1](bob-cli-7b.1.md) | 2026-10-13 09:24:19 EDT |
| bob-cli | [`bdfc8c3`](https://github.com/bobs-org/bob-cli/commit/bdfc8c3ee3edb5eef6f3ba0dddc12c36ef8095ec) | feat(capture): route toggle, ensure-next and link-then-close through shared link guard | [bob-cli-7b.2](bob-cli-7b.2.md) | 2026-10-13 10:14:59 EDT |
