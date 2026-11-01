# Bead: bob-cli-fb — Keep leaf projects moving — offer a sub-project's ready tasks when its last planned task closes

[Bead Pages](../README.md) / bob-cli-fb

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bz](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bz.md) · **Assignee:** `bob-cli-fb.land`
**Created:** 2026-11-01 12:29:36 EST
**Plan:** [202611/leaf\_project\_keep\_moving\_offers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/leaf_project_keep_moving_offers.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/leaf_project_keep_moving_offers.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/leaf_project_keep_moving_offers.md

<!-- sase:links:end -->

## Description

When any managed Done gesture, on any surface, closes the task behind a leaf project's last live Task Link in today's Pomodoros, Bob offers that project's ready tasks in one picker. The picker says plainly why it appeared and that the rows are not dependents. Rust and the JS cycler apply one rule, pinned by shared vectors. Obsidian, `bob capture`, and Bob Mac Capture present it with one copy and visual system.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-fb.1](bob-cli-fb.1.md) | Contract, glossary, and docs | ✓ closed | medium | 2026-11-01 | 1 | 1 |
| [bob-cli-fb.2](bob-cli-fb.2.md) | Rust engine and capture reporting | ◐ in_progress | large | 2026-11-01 | 1 | 0 |
| [bob-cli-fb.3](bob-cli-fb.3.md) | Obsidian picker and notice presentation | ◐ in_progress | medium | 2026-11-01 | 1 | 0 |
| [bob-cli-fb.4](bob-cli-fb.4.md) | Obsidian cycler engine | ◐ in_progress | large | 2026-11-01 | 1 | 0 |
| [bob-cli-fb.5](bob-cli-fb.5.md) | Bob Mac Capture presentation | ◐ in_progress | medium | 2026-11-01 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-fb: Keep leaf projects moving — offer a sub-project's ready tasks when its last planned task closes [in_progress]"]
    n1["bob-cli-fb.1: Contract, glossary, and docs [closed]"]
    n2["bob-cli-fb.2: Rust engine and capture reporting [in_progress]"]
    n3["bob-cli-fb.3: Obsidian picker and notice presentation [in_progress]"]
    n4["bob-cli-fb.4: Obsidian cycler engine [in_progress]"]
    n5["bob-cli-fb.5: Bob Mac Capture presentation [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n1 -.-> n2
    n1 -.-> n3
    n1 -.-> n4
    n2 -.-> n5
    n3 -.-> n4
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-fb.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fb.1/README.md) | [bob-cli-fb.1](bob-cli-fb.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-fb.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fb.2/README.md) | [bob-cli-fb.2](bob-cli-fb.2.md) | 0 |
| [bbugyi200.apollo.bob-cli-fb.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fb.3/README.md) | [bob-cli-fb.3](bob-cli-fb.3.md) | 0 |
| [bbugyi200.apollo.bob-cli-fb.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fb.4/README.md) | [bob-cli-fb.4](bob-cli-fb.4.md) | 0 |
| [bbugyi200.apollo.bob-cli-fb.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fb.5/README.md) | [bob-cli-fb.5](bob-cli-fb.5.md) | 0 |
| [bbugyi200.apollo.bob-cli-fb.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fb.land/README.md) | [bob-cli-fb](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d6b16f4`](https://github.com/bobs-org/bob-cli/commit/d6b16f4f42553ec186a1846537e655714d11839f) | docs(keep-moving): pin leaf-project contract, copy, and vectors | [bob-cli-fb.1](bob-cli-fb.1.md) | 2026-11-01 12:49:50 EST |
