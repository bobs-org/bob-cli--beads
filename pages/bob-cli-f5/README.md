# Bead: bob-cli-f5 — Task link marks — status rings on links that point to tasks

[Bead Pages](../README.md) / bob-cli-f5

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.16q](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.16q.md) · **Assignee:** `bob-cli-f5.land`
**Created:** 2026-11-01 09:24:20 EST
**Plan:** [202611/task\_link\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_link_marks.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/task_link_marks.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_link_marks.md

<!-- sase:links:end -->

## Description

Every rendered link whose target is a `#task` line wears a small status ring (Ready, Next, In Progress, Blocked, Done, Cancelled) in Live Preview and rendered views, so Bryan can tell at a glance which links point to tasks and what state those tasks are in. Links to notes, headings, and non-task blocks stay exactly as they are, nothing is ever written to the vault, and a session toggle restores plain links.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-f5.1](bob-cli-f5.1.md) | Contract, pure core, ring glyphs, and visual preview | ✓ closed | medium | 2026-11-01 | 1 | 2 |
| [bob-cli-f5.2](bob-cli-f5.2.md) | Live Preview rings, resolver, refresh, and toggle | ✓ closed | medium | 2026-11-01 | 1 | 2 |
| [bob-cli-f5.3](bob-cli-f5.3.md) | Reading view, embeds, hover popovers, and query rows | ✓ closed | medium | 2026-11-01 | 1 | 1 |
| [bob-cli-f5.4](bob-cli-f5.4.md) | Real-Obsidian e2e, docs, version, and sync | ✓ closed | medium | 2026-11-01 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-f5: Task link marks — status rings on links that point to tasks [in_progress]"]
    n1["bob-cli-f5.1: Contract, pure core, ring glyphs, and visual preview [closed]"]
    n2["bob-cli-f5.2: Live Preview rings, resolver, refresh, and toggle [closed]"]
    n3["bob-cli-f5.3: Reading view, embeds, hover popovers, and query rows [closed]"]
    n4["bob-cli-f5.4: Real-Obsidian e2e, docs, version, and sync [closed]"]
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
| [bbugyi200.athena.bob-cli-f5.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-f5.1/README.md) | [bob-cli-f5.1](bob-cli-f5.1.md) | 2 |
| [bbugyi200.athena.bob-cli-f5.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-f5.2/README.md) | [bob-cli-f5.2](bob-cli-f5.2.md) | 2 |
| [bbugyi200.athena.bob-cli-f5.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-f5.3.md) | [bob-cli-f5.3](bob-cli-f5.3.md) | 1 |
| [bbugyi200.athena.bob-cli-f5.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-f5.4/README.md) | [bob-cli-f5.4](bob-cli-f5.4.md) | 1 |
| [bbugyi200.athena.bob-cli-f5.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-f5.land/README.md) | [bob-cli-f5](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a1233eb`](https://github.com/bobs-org/bob-cli/commit/a1233eb8f4fa3bded9df99d3f289328b15e1681f) | feat(task-link-marks): display contract, registry, and docs links | [bob-cli-f5.1](bob-cli-f5.1.md) | 2026-11-01 09:49:06 EST |
| bob-plugins | [`bob-plugins@a67b8cd`](https://github.com/bobs-org/bob-plugins/commit/a67b8cddff9b4638e4b4c2342642063ef176c77b) | feat(task-link-marks): pure core, ring CSS, preview, and conformance tests | [bob-cli-f5.1](bob-cli-f5.1.md) | 2026-11-01 09:49:22 EST |
| bob-cli | [`4ea4c33`](https://github.com/bobs-org/bob-cli/commit/4ea4c330df72b32c20bb91ec4a5440f8edab6a72) | docs(task-link-marks): name the Live Preview fragments and swap class | [bob-cli-f5.2](bob-cli-f5.2.md) | 2026-11-01 10:11:12 EST |
| bob-plugins | [`bob-plugins@13d40ac`](https://github.com/bobs-org/bob-plugins/commit/13d40ac4ec851f0f60cae581a21d581157fc0d07) | feat(task-link-marks): Live Preview rings, resolver, refresh, and toggle | [bob-cli-f5.2](bob-cli-f5.2.md) | 2026-11-01 10:11:28 EST |
| bob-plugins | [`bob-plugins@bedc7e2`](https://github.com/bobs-org/bob-plugins/commit/bedc7e2a7cb16257b48bc3b26241d663a2f161db) | feat(bob-ledger-tools): mark task links in reading views | [bob-cli-f5.3](bob-cli-f5.3.md) | 2026-11-01 10:42:18 EST |
| bob-plugins | [`bob-plugins@32c9e03`](https://github.com/bobs-org/bob-plugins/commit/32c9e03248a03c1570f4dea6a29e7c8f6c15f130) | feat(task-link-marks): land rings in real Obsidian and bump 1.81.0 | [bob-cli-f5.4](bob-cli-f5.4.md) | 2026-11-01 11:23:08 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-f5.1][1] | Need epic context for phase f5.1 | 1 |
| read-by | [agent:bob-cli-f5.2][2] | Epic context and phase notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-f5.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-f5.2/README.md

<!-- sase:referenced-by:end -->
