# Bead: bob-cli-bk — Capture asks where inbox tasks go

[Bead Pages](../README.md) / bob-cli-bk

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.a9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.a9.md) · **Assignee:** `bob-cli-bk.land`
**Created:** 2026-10-24 14:00:26 EDT
**Plan:** [202610/capture\_inbox\_routing.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_inbox_routing.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/capture_inbox_routing.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_inbox_routing.md

<!-- sase:links:end -->

## Description

Every capture that changes the status of an existing inbox task makes Bob Mac Capture ask which area or open project the task belongs in, and bob applies the capture and the move in one atomic batch.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-bk.1](bob-cli-bk.1.md) | Detect inbox route candidates and refuse without a choice | ✓ closed | medium | 2026-10-24 | 1 | 1 |
| [bob-cli-bk.2](bob-cli-bk.2.md) | Apply inbox route answers inside the capture batch | ✓ closed | medium | 2026-10-24 | 1 | 1 |
| [bob-cli-bk.3](bob-cli-bk.3.md) | Decode inbox routes and send route answers in CaptureCore | ✓ closed | medium | 2026-10-24 | 1 | 1 |
| [bob-cli-bk.4](bob-cli-bk.4.md) | Route card in the Bob Mac Capture panel | ✓ closed | medium | 2026-10-24 | 1 | 2 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-bk: Capture asks where inbox tasks go [in_progress]"]
    n1["bob-cli-bk.1: Detect inbox route candidates and refuse without a choice [closed]"]
    n2["bob-cli-bk.2: Apply inbox route answers inside the capture batch [closed]"]
    n3["bob-cli-bk.3: Decode inbox routes and send route answers in CaptureCore [closed]"]
    n4["bob-cli-bk.4: Route card in the Bob Mac Capture panel [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n1 -.-> n2
    n2 -.-> n3
    n3 -.-> n4
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-bk.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bk.1/README.md) | [bob-cli-bk.1](bob-cli-bk.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-bk.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bk.2/README.md) | [bob-cli-bk.2](bob-cli-bk.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-bk.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bk.3/README.md) | [bob-cli-bk.3](bob-cli-bk.3.md) | 1 |
| [bbugyi200.apollo.bob-cli-bk.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-bk.4.md) | [bob-cli-bk.4](bob-cli-bk.4.md) | 2 |
| [bbugyi200.apollo.bob-cli-bk.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bk.land/README.md) | [bob-cli-bk](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`bb52dd0`](https://github.com/bobs-org/bob-cli/commit/bb52dd0ab1c5d947a84b2c98f6e29620c7a3e7ff) | feat(capture): detect inbox route choices | [bob-cli-bk.1](bob-cli-bk.1.md) | 2026-10-24 14:58:27 EDT |
| bob-cli | [`4f13e97`](https://github.com/bobs-org/bob-cli/commit/4f13e979eb3dba1a69c840bfb2c34a9d0ff7ecd6) | feat(capture): route inbox answers through task-move engine | [bob-cli-bk.2](bob-cli-bk.2.md) | 2026-10-24 16:34:24 EDT |
| bob-mac-capture | [`bob-mac-capture@2968311`](https://github.com/bobs-org/bob-mac-capture/commit/2968311e5fa7924ed99bf83e52df865ee6e114c1) | feat(mac-capture): decode inbox routes and send route answers in CaptureCore | [bob-cli-bk.3](bob-cli-bk.3.md) | 2026-10-24 17:16:02 EDT |
| bob-cli | [`e70f9ea`](https://github.com/bobs-org/bob-cli/commit/e70f9ea40a7be87ffc761b851eda2613d288e9c8) | docs(memory): explain capture inbox routing | [bob-cli-bk.4](bob-cli-bk.4.md) | 2026-10-24 18:10:17 EDT |
| bob-mac-capture | [`bob-mac-capture@7bfa312`](https://github.com/bobs-org/bob-mac-capture/commit/7bfa31275b3dccbb72e15f664065bddd8363a39d) | feat(capture): add inbox route card | [bob-cli-bk.4](bob-cli-bk.4.md) | 2026-10-24 18:11:20 EDT |
